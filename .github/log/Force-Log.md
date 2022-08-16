# Force-Log

0.3.5 to 0.4.0:   
	- Scripting: Expands the Scripting API (Debug, GameObject), add Window, PrimitiveType, Utils, Vector2i, Vector2i.   
	- Scripting: Major scripting update. Now all core of C# library stores in different module ForceCSCore.dll that now links to user scripts file ForceCS.dll.   
	- Scripting: Now project link the ForceCSCore.dll directly to EditorPath.
	- Project: Add to config EditorPath and LastEditorPath to save the editor path for linking other dynamic libraries.   
	- SceneManagment: Fix bugs with scene manager, replace RemoveByAddress on Unload for removing scene from memory.   
	- SceneManagment: Add support for sorting gameobject node by name, uuid, transform.   
	- Core: Element System: Improve the element system, add category for element and advanced callaback sending via ElementCallbackClass.   
	- Scripting: Starting work on SceneManager API for script, add Scene.cs and SceneManager.cs classes, and now C++ SceneManager has termin of scenes that was created by script at runtime.   
	- Inspector & Explorer: Components View now will displayed specific for Edit Mode and Runtime Mode. In runtine when we select object on scene from script Explorer will send the context to Inspector.   
	- Core: Application System: Replace old Config class by new ApplicationSpecificaion.   
	- Core: Application System: Add ApplicationCmdArgsSpecification, ApplicationWindowSpecification. Now application knows about its worlking path and resources directory.   
	- Runtime: Add new ForceRuntime project. This project will used to play final excecutable project/product.   
	- Core: Application System: Add ApplicationUserSpecification instead of Project::ProjectConfig. Remove Project::ProjectConfig.   
	- Core: Application System: Now instead ForceConfig.json Force creates ForceUser.json from ApplicationUserSpecification.   
	- Runtime: Start working on integration playable runtime application. Starts with RuntimeElement.   
	- Runtime: Completed playable runtime application. Now at this point user project that created in Editor can be run inside Force Runtime shell, and be kinda executable.      
    - Runtime: Now runtime application have two state of excetution, one is when we run in IDE (search by start project path and use ForceUser.json), and second is final game app (all assets, resources and paths relative to game .exe file).   
	- Runtime: Add support for raw application exporting in Force Editor (Build), only throw Force solution, other no have any idea how to implement.   
	- Platform: Window: Add support for maximize window for ShowWindow function, add PayWindowAttention funtion.   
	- Editor: Add Platfrom Configuration settings and Scenes Build settings. Now this settings does nothing.   
	- Platform: Window: Add support for dark mode. Win32 API: Expose uxtheme.dll functions. GLFW: Not supported by its core.   
	- Editor: Fix the white theme in some places with incurrect colors.   
	- Core: Application System: Application now can runs without ImGui context and element. Add ApplicationPlatformSpecification.   
	- Platfrom: Window: Add MouseCursorType enum. Win32: Fix not even loaded cursor. (Founds out when remove ImGuiElement and test without it.).]
	- Core: Application System: Refresh, redising, update, remove unnessisary code.   
	- Platform: Now platform detects not as part of Application, but part of each OS Entry Point.   
	- Scripting: Now scripting backend initialize not by Application, by platform Entry Point. Because Mono JIT cannot be reloaded if it was CleanUp.   
	- Graphics: Match all graphics creation code to PlatfromLibraryAPI.   
	- D3D10/D3D11: Fix the bug with not setted primitive topology, to render all primitives as lines not triangles.   
	- Platfrom & Debug: Match ImGui Element by PlatformLibraryAPI. Graphics: Also PlatfromAPI was renamed to RendererAPI, and the same with FE_RENDERER_ macros.   
	- Editor: Add renderer support for building. Uncomplited.   
	- Core: Application System: Update the application system, add Core.h/cpp files that initialize the core systems. Improve closing via new Shutdown function. Now application update loop is updates by running flag not by window->IsCloseRequested.   
	- Nave: Starting working on super simple Launcher for Force (Force Nave).   
	- Core: Now user can use ManagedInitializeCore() to disable Core engine.   
	- Core: Application System: Now user can disable rendering and audio engines. (But it will still links and requrie DLL's.)   
	- Nave: Raw implement the Force Builds (Installs) property.   
	- Core: Application System: Add ApplicationVersionFlags to decompose the compared version by Application::CompareVersion().   
	- Localization: Move language system to Force Engine from Editor and rewrite it to be accessable for Nave.   
	- Nave: Implement the Installs and documentation pages. Working on Projects Tab.   
	- Nave: Implement Projects Tab. Force Builds now can be opened. Improve Installs tabs.   
	- Serialization: Write new Wrapper YAML API based on YAML.   
	- ImGui: Editor and Nave now save imgui configs not imgui.ini, but in Resources/Application/GuiSettings.ini.   
	- Other: Add the ResourceScript.rc for each project and output executable now have its icons.   
	- Core: Application System: ApplicationBootSpecification now accept list of arguments that comes from cmdlineArguments.   
	- Editor: Add way to load project that comes from cmdLineArguments if not load with standard way.   
	- Nave: Implement Open Project/Force button and loading Force with selected project and without it.   
	- Input: Fixed bug with Creating input as Ref but also deleting raw pointer at initialization/deinitialization.   
	- Nave: Add Tabs icons, add Create Project Tab.   
	- Graphics: Add .ShaderCache, that now contains all in-build engine shaders for renderers. Shaders now load in-build default shaders if user not provide custum implemention.   
	- RenderEngine2D: Add asserts if we trying to render primivites outside the scope Begin() - End(), or if we call End/Begin to many times. If we call one of render function outside scope this primitives will be skipped.   
	- Math: Few refactoring in math for current Force API. Add GetTransform(), GetView() functions for common usage.   
	- RenderEngine2D: Fix bug the renderer not free vertex buffer/index buffer from GPU.   
	- Graphics: Major graphics clean-up and refactoring. See Force-Log_RendererRefactoring.md for details.   
	- IO: Move IO module from Force::Core to Force::IO, now its indemendent module.   
	- Graphics: GL: D3D: Fix the Uniform buffer binding index, blocks situation again. Now its should work in all cases.   
	- Graphics: Rewrite Model and Mesh classes and Face, add MaterialTextureType, restore basic 3d renderer and loading model via new API.   
	- RenderEngine: Clean-up and rewrite the 3D renderer, restore it at that state where we can render something with it.   
	- Examples: Add the new ExampleApplication Project to test core and rendering in future. This example is explaned in docs on For Engine Developers page.   
	...
0.3.5:   
	- SceneManagment: Fix saving scene with incurrect name.   
	- Project: Fix saving project with current scene not make it startup.   
	- Editor: Fix bug when attach another script to object, not displayed add button.   
	- Scripting: Now all prefabs instantiate staticaly before copy scene objects to mono.   
	- Editor: Fix bug with incurrect viewport resizing at start of runtime scene.   
	- Scripting: We dont need to set the 'ratio' from Mono.   
	- Scripting: Support for multiple camera holding and switching between them.   
	- Scripting: Fix bug with writing updated camera projection.   
	- Graphics: UniformBuffer: Add function SetBuffer to pass raw data to shader buffer.   
	- Scripting: Add Shader, ShaderBufferBlock, StructuredBuffer, Math, Color, Color32 classes to deal wtih shaders and colors. BETA commit.
	- RenderEngine2D: Fix bug with using three identical buffers of VP to one, and remove shaders binding when upload data in Begin().   
	- UniformBuffer: GL: Fix bug: OpenGL uniform buffer was not realocate the buffer when pass data with different size in PutData() and SetVariable().   
	- Scripting: Add functionality to create a uniform buffers (ShaderBuffers/Blocks) throw script using Shader.CreateBlock() and dynamically set the data by Shader.SetBuffer().
	- Scripting: Fix bug with recompiling assembly when binary file actually locked by another procces.   
	- Scripting: Fix issues with Color, Color32, and Vectors beeing rendered in inspector and update values.   
	- Audio: Starting to implementing the Audio system for Force. Add AudioContext, SoundBuffer, SoundSource, AudioEngine per platfom classes with backend OpenAL.   
	- Audio: Add SoundSourceSpecification and make some chanages in AudioEngine.   
	- Audio: Add support for .ogg, .mp3, and other formats sound loading with sndfile library. Add test playing and test streaming.   
	- Audio: Add Sound class for streaming sounds with multiple buffers working nicely.   
	- Audio: Upgrade AudioEngine to support loading streaming and non-streaming audios.   
	- Audio: Implement Stop() function and add way to pause source in Play() function.   
	- Audio: Add SoundListener class. Add way to change the position, gain, and velocity of the Mono sound.   
	- Editor: Add way to loading and playing audio clips in editor throw new editor audio inspector UI.   
	- Editor: Upgrade Audio Clip Manager and localized it.   
	- Editor: Add playback timer to Audio Clip. Add Script & Prebab file managers to preview the assets.   
	- SceneManagment: Add AudioClip, AudioSource & AudioListener components + serialization. Each new scene have by default AudioListener attached to position of camera.   
	- Editor: Make a UI for AudioSource & AudioListener components.   
	- Editor: Settings: Add new Audio Settings manager, that allow controll the global editor playback of clips.   
	- Editor: Create new Tag Manager.   
	- Editor: Add Scene icon and name of it in Explorer with it state.   
	- Editor: Add to project browser settings with context type.   
	- Editor: Fix bug with reseting components at runtime.   
	- Scripting: Add AudioClip, AudioSource, AudioListener components to C#. User now can play sounds using script. Not all features is present.   
	- Editor: Fixed ton of bugs in ProjectBrowser with renamed dirs, and input box. Add/Remove components now set SceneChanged on true.   
	- Scripting: Add AudioListener implementation. Fix AudioSource fields.   
	- Build: Tested current build on Release.   
	- Project: Add the Build settings and Visual Studio paths.   
	- Scripting: Now .cs files builds automatically on Play without Visual Studio.   
	- Utils: Win32: Add support for Toolbar ProgressBar.   
	- Editor: Add new GameObject Icon on Explorer.   
	- Editor: SceneExplorer: Add new settings button with scene options, loading, unloading, set as editable, etc.   
	- Editor: ProjectBrowser: Add buch of fixes, and add new popup on black space and on item space click.   
	- Editor: SceneExplorer: Add new menu if none of scenes is not loaded.   
	- Editor: Add multiple scene holding and editing. Now user can edit multiple scenes and save it at the same time and play it.   
	- Editor: Update explorer panel, add new buttons and popup-UIs.   
	- Editor: Add scene loading-unloading state, now scenes can be unloaded and stay in explorer or loaded back, and then deleted.   
	- SceneManagment: Add camera background field.   
	- Editor: Settings: Add new Profiler & Colors setting tabs.   
	- Editor: Add colored outlines for selected objects.   
	- RenderEngine2D: Expand the renderer and add the RenderGrid() function to render grid of lines.   
	- RenderEngine2D: In line renderer now lines check on depth.   
	- Editor: Add the 2D Mode button and Alt/Block/Alt modes when in 2D mode. 2D Mode button make the 2D view of scene.   
	- Platform: Add the DragDrop class. Win32: Add DragDropWin32 class.   
	- AssetManagment: Preparing for Asset System. Force now tracks that Assets folder was changed, add add grag & grop files from system (OS) explorer to project browser.   
	- AssetManagment: Starting to implement Asset System.   
	- AssetManagment: Add reimport assets. Starting to implement Image Asset type description.   
	- Editor: Add visual representation of Asset Manager and assets via Inspector. Begin with Image Asset.   
	- Editor: ProjectBrowser: Now he displaying images instead old file icon.   
	- Graphics: Texture: Add TextureType enum class. Add conversion between other texture enums.   
	- AssetManagment: Add renaming with keeping the same UID, and removing asset to "Backup" or removing it completle.   
	- AssetManagment: Assets now automatically reimports when some of it changes inside the Editor. Note: If asset removes/renames outside the Force it break the asset and it UID and create new asset with new UID.   
	- Editor: Fix the Browser OS drag-drap rectable.   
	- Editor: Add custom implementation of slider using ImGui.   
	- Editor: ProjectBrowser: Update design.   
	- Editor: Console: Update design and information about saving project & scenes.   
	- Graphics: Texture: Fix the incurrect filter1 value was not passing in the specification.   
	- Graphics: Texture: Update the DymamicTextureSpecification & TextureFilterType API.   
	- AssetManagment: Extend the Asset & AssetManagment to support loading, saving the Image type assets.   
	- SceneManagment: SpriteRenderer Component now accept the assetUID not filepath.   
	- Editor: Add Drag & Drop and UI for Image Asset.   
	- Editor: Fix incurrect offset of buttons, redesign the some widgets and style.   
	- Editor: Add support for components moving up and down.   
	- AssetManagment: Now if .ext file exist, but local file not it will attempt to load this asset.   
	- AssetManagment: Image asset load texture when it file is appears in Assets, if not show message Missing.   
	- AssetManagment: Starting to implement Image Audio type.   
	- Editor: Add visual representation of Audio Asset.   
	- AssetManagment: Fix bunch of issues with Audio & Image asset and improve it.   
	- Editor: ProjectBrowser: Fix uncorrect drag-drop icons event.   
	- Editor: ProjectBrowser: Remove refresh and open folder buttons. Add new sub-panel.   
	- AssetManagment: Upgrade the asset manager and fix issues in some functions.   
	- Editor: ProjectBrowser: Start working on draging items to folders. (Not working if file is opened by another proccess).   
	- Editor: ProjectBrowser: Fix bugs with dragging state and audio files.   
	- Editor: ProjectBrowser: Add support for moving files in back directory (displayed with new icon).   
	- AssetManagment: Add CreateAsset function. And fix bugs #0073 & #0074.   
	- Editor: ProjectBrowser: Fix bugs with folder assets. And fix  #0075 & #0076 & #0077.   
	- AssetManagment: Add support for removing complex assets. Add RemoveLinkedAssets(), PushLastAssetIndex(), PopLastAssetIndex().   
	- AssetManagment: Add support for moving complex assets. Moving folder asset to anohter folder.   
	- Editor: ProjectBrowser: Add new button Copy and Paste asset.   
	- AssetManagment: Add support for renaming assets. Complete.   
	- AssetManagment: Add visual representation of Scene Asset. Scenes now can be opened from asset.   
	- Editor: Add Scene Dialog window for creation scenes. Now scenes create as asset.   
	- AssetManagment: Now asset manager skip hidden special OS files/folder starting with "." or ends with "~".   
	- AssetManagment: Starts working on CSharp Script Asset.   
	- AssetManagment: Now scripts can be draged on dropped as actual asset.   
	- Editor: Regesign the CSharpScriptComponent UI for asset button.   
	- Scripting: Little rewrite MonoBackend for assets scripts.   
	- Scripting: Now EditorElement has global BuildScriptEngine function that eventially do all work with compiling, moving ForceCS.dll files and compiling to Mono scripts.   
	- SceneManagment: SceneSerializer: Add root header as Force version, and Serializeble Version for scene, that scenes can detect if feature version of Force update SceneSerializer, and block loading scenes if scene version < Serializeble Version.   
	- AssetManagment: Starts working on Prefab asset.   
	- Editor: Add support to dragging prefabs in to Explorer with highlight.   
	- Scripting: When moving script file to another folder (In Assets) it automatically regen the script project. (If moving folder -> scripts not working).   
	- Editor: Add Prefab Dialog window for creation prefab. Now prefabs create as asset.   
	- Win32 + ImGui: Add support for dialog window renders as normal Win32 windows and block parent window.   
	- Editor: Add new dialog windows for opened project and scene. Add project name on top on menu bar.   
	- Editor: Refacting the Menu Bar, now Play,Stop buttons not part of dockspace. Add new StatusBar panel.   
	- Editor: Add Copy & Paste components in component settings.   
	- Scripting: Fix bug when call one of Find_() methods its return new instance to C# object not that witch exist in monoGameObjects, and its block opportunity to change object in script.   
	- Editor & Scripting: Upgrade the prefab system. Now prefabs can be automatically init by Force or manially by user in script.   
	- Build: Update the build and SMI configurations.   
	- AssetManagment: Starts working on brand new Preset asset.   
	- SceneManagment: Split the component serialiation to SerializeComponent/DeserializeComponent functions. (For Preset System)   
	- Editor: Inspector: Split component drawing by types. ByRegistry, ByInstance. Add new drawing component type, its ByInstance (directly access to component without using the GameObject). (For Preset System)   
	- Editor: Add Preset Drag Drop.   
	- Editor: Add Physics Simulation Mode.   
	- Scripting: Fixing bug that GameObject that was created from script not send its components data to Force.   
	- Scripting: Fixing bug that GameObjects transforms and physical data not currenlty updates to/from Mono.   
	- Scripting: Fixing bug data not send to Mono after OnStart().   
	...
0.3.0a:   
	- Core: Update ForceML. Added new Typed^ types of vector to easy indentify it and recreate Vector^ operators. Status: in progress.   
	- Graphics: Refactoring in VertexArrayObject, VertexBufferObject, IndexBufferObject, replace create(), destroy() functions by constructors and destructor.    
	- Core & Window: Fix nasty bug when engine crashing on window exit button or randomly when using PlatformApplication::Exit() function.   
	- Graphics: GL: Wrap some function in FE_GLCALL(...) with basic glGetError(). GL4: Add modern debug support with GL_DEBUG_CONTEXT. And made a lot of changes in other 
	Graphics files.   
	- Editor: New beta Project System.    
	- Core: Remove from GraphicsAPI.cpp / RenderEngineHelper.cpp commented preprocessor platform defines + add if statement to check define dynamic API and create 
	FE_GRAPHICS_API_DEFAULT macro in PlatformApplication.h.   
	- Core: Remove Render*RotWith* API from RenderEngine2D.h.   
	- Editor: Add Project Browser Panel + Finished Project System. Now user can load projects/scenes and save it on disk. 
	- Core: Add IDStack concept, and refresh BasePanel.h file.   
	- Editor: Fix Console Panel on delete + Fix Settings Panel.   
	- Editor: Fix dymanic changing theme.   
	- Editor: Add new 'Editor Beta Features' & 'Font Size' settings. Finally fix all bugs and/with style with ProjectSettingsPanel.  
	- Editor: Add opportunity to open scene from Drag & Drop. Optimize the Project Browser Panel.   
	- Editor: Add Search filter and add texture using Drag & Drop. Refreshing the API.   
	- Editor: Add dynamic Window X System change from Editor option in Graphics Settings. Window: Add TitleFlags to construct default title.   
	- Platfrom: Remove platform init from window / context classes, and create seperate files for each platform that will init all .dlls / functions specific for that platform.   
	- Platform: Remove Force::Window namespace (renamed PlatformWindow to Window), all classes moved to Force::Platform::/GLFW/Win32 namespaces.   
	- Platform: Moved (renamed PlatformTimer to Timer) to Force::Platform namespace with GLFW/Win32 implementations.   
	- Core: Renamed PlatformApplication to Application for simpleset.   
	- Platform: Updating the Win32 Library.  
	- D3D11: Add mipmapping support for textures. 
	- UniformBuffer: Add Upload() function and UploadAndSet() function to manually set uniform and then upload in GPU if requries.   
	- D3D11: Add support for Framebuffers (RenderTargetView + Texture2D + ShaderResourceView).  
	- Graphics: Add RenderCmd::CullMode & RenderCmd::SetCounterClockwise API for OpenGL & DirectX 11.   
	- UniformUploader: Add SetVector(), SetFloat() & SetInt() functions. Uniform Buffers now at working stage.   
	- Graphics: Add UniformBlock and UniformUploader API. Sonner will replace old Shader loading unfiorms API. D3D11 & GL: Now supports multiple buffers loading, but some problems has with OpenGL.   
	- D3D11: Add in Win32 proc WM_SIZE DirectX 11 SwapChain resizing. Add almost full integration ImGui with DirectX 11 (Docking & Viewport_Enabled).   
	- Core: Add UUID system. D3D11 & GL: Fixed not renderable texture in shader.   
	- SceneManagment: Add CreateObjectWithUUID() and diserizliztion for UUID. Core: Add beta Reload() func in FE_EXPEREMENTAL. D3D11: Starting to implement mipmapping.   
	- D3D11: Add D3DImage and GDIPlus to load textures using GDI, not throw WIC or DSS. Also fixed texture filtering, and add new combined filter flags.   
	- Graphics: Added TextureWrappingMode platfrom structure. D3D11: Framebuffer now support multiple render targets rendering. And fix the ReadPixel() function, now you can select object from scene by clicking on it.   
	- Editor: Refact the UI Play/Stop/Pause/Resume buttons, recreate hole framebuffer switching/resizing situation in EditorElement.cpp and create SceneState structure.   
	- Physics2D: Add the Box2D physics library and interate it to the editor with BoxCollider2DComponent and RigidBody2DComponent. And serialize-desirialize this components.   
	- Editor: Fix the ImGuizmo rotation bug with uncurrect text formating.   
	- Editor: Add scene Copy functions and CopyComponent to reset the scene and switch to editor scene when not playing and then back to runtime if we play.   
	- Editor: Add EditorCamera free moving. (Early test)   
	- Build: Add python scripts to automatically download all additional resources want we need and generate project on Windows, insted of old CMI.bat on Batch.   
	- SceneManagment: Project and Scenes open functions now use the Path(std::path) instead of String(std::string). Add check filepath on extensions.   
	- Physics2D: Add more paramteters to RigidBody2DComponent such a mass, inertia, gravityScale, gravityVelocity etc.    
	- SceneManagment: Add to SceneSerializer.cpp Get and Set templates functions to automatically set values if in the that not exist.   
	- Physics2D: Add 'simulated' param to BoxCollider2DComponent. Dont create Physics2D World if no object in scene hasnt 2D components.   
	- D3D10: Implement fully functional DirectX 10 Graphics API for older GPU's, like GL3.3.  
	- Platform: Add new FE_PLATFORM_WINDOWS_WINx macros to determine extatly witch version of Windows we need use to compile code. For example if we compile to Win7 we not want to use d3d12.lib at all and all D3D12 code.  
	- RenderEngine2D: Add circle renderer and CircleRenderer component.   
	- RenderEngine2D: Remove a lot of RenderRectangle unused overloads functions. 
	- Physics2D: Added the Circle2DCollider component and circle physics.  
	- RenderEngine2D: Add line renderer and line rectangle renderer.   
	- Editor: Add new components to menu bar, add icon to component settings, add reset button to reset components.  
	- Editor: Add visual camera sprite that renders on camera position, and add visual camera aspect.   
	- Scripting: Add test Mono integrations and create ForceCS project in C# to create scripts. For now not working with premake5.lua.   
	- Editor: Add visual debug rendering for box and circle colliders.   
	- Editor: Add the controll list in settings panel to see all keys using in Force.   
	- Build: Add Python Mono script, and optimize the compilation.   
	- Core: Add header include for each Force Module, like Force_Core or Force_Scripting.   
	- Core: Add ForceExceptionCallback and SetExceptionCallback function.   
	- Editor: Add new setting group and new settings: OpenLastProject, Autosave, SaveOnExit.     
	- Core: Add ResolutionTimer.h class to simple run the timer and measuare time in seconds.   
	- Editor: Add the new Dialog Boxes to ProjectManager is scene/project not loaded.   
	- Editor: Fix text input and camera moving at the same time.   
	- Editor: Add new component icons and refact/fix size of others.
	- Core: Add new HandleException() function.   
	- Editor: Fix all text inputs, fix not updating project info data when project is loading, add close buttons on some panels.   
	- Editor: Add Undo/Redo system for Create/Destrying Objects, Transform, Colors, Textures, Copy & Paste & Duplicate commands.    
	- Editor: Add panels reseting & new icons/redesize old.   
	- SceneManagment: ECS now has Unsafe function create by me, without assert if entity is not valid for Undo/Redo system.   
	- Editor: Update the Console Panel.   
	- Scripting: Add almost full intergration C# scripting: Debug, Input, GameObject and Components integration. Only for now Force not support runtime recompilation scripts/assemblies.   
	- Scripting: Add a lot of functionality to script system. Now script can hold: OnCreate(), OnStart(), OnUpdate(), OnPreRender(), OnRender(), OnPostRender(),OnRenderGUI(), OnDestroy() events.   
	- Scripting: Add EditorPanel class as wrapper over ImGui. Usage of it is just debugging with UI throw script.   
	- Scripting: Add Matrix4, Matrix3 and RenderEngine2D classes. Throw this in OnRender() you can render primitives throw script.   
	- Scripting: User now can create / copy objects throw scripts. Now MonoScript stores all objects created in script in runtime.   
	- Scripting & Editor: All basic type field now can be displayed in Inspector and user can change. Scripts now can be created in custom namespace.   
	- Scripting: Script engine now full dynamically recompiled. 98procents of crashes is gone.   
	- Scripting & Editor: Add new prefab type support. Users can create prefabs and attach it to script in inspector.   
	- Editor: Upgrade the ProjectBrowser Panel.   
	- Editor: Settings: Add new Build setting that hold info about how sould build project.   
	- Editor: Settings: Add new User (preparing for exporting Application now this does nothing).   
	- Editor: Add UI for creating script files.   
	
0.2.5.8 - Graphics: WGL: Add more funtionality to Win32 WGL Context.    
0.2.5.7 - Editor: Settings, Language and imgui.ini files are now creates automatically if its not on the disk.
0.2.5.6 - Graphics: GL3: Fix bug: Doesn't render textures in batch renderer.  
0.2.5.5 - Graphics: GL3: Now framebuffer support it, and render all currectly. RenderEngine2D: GL3: Doesn't render textures in batch renderer since 0.1.20.3.7c.   
0.2.5.4 - Graphics: GL4: Recreate Framebuffer API, now is more structured and support easing attaching Render Targets. GL3: Framebuffer doesnt render anything, black texture.   
0.2.5.3 - Graphics: Written new GLH API instead old one GLHelper, now is more usable and not recall gl functions.    
0.2.5.2 - Win32: WGL: Fully recreate WGL context, now all WGL_CONTEXT_CORE_PROFILE_BIT_ARB, WGL_CONTEXT_COMPAT_PROFILE_BIT_ARB, WGL_CONTEXT_FORWARD_COMPAT and WGL_CONTEXT_DEBUG_BIT_ARB works perfectly with all extensions.    
0.2.5 - Editor: Add preview of runtime view in editor. And add 'play' button to runs the scene-application and stopping it by pressing escape.   
0.2.4.3 - Window: Fix uncorrect title when new scene is created, displayed old scene title.   
0.2.4.2 - Graphics: RenderEngine2D: Add support for 'Selection' of GameObject's using objectID as vertex buffer attribute to determite pixel on screen as id or empty space.   
0.2.4 - Graphics: RenderEngine: Add the EditorCamera class, and now editor scene will render throw that camera. Also Rewrite the RuntimeCamera class. Editor: Add control buttons to easy changing the gizmo types and EditorCamera projection.   
0.2.3.12 - Editor: Add snapping to Gizmos using Alt/Alt+Shift when moving. Fixed shifting the Gizmo model itself in other game objects.   
0.2.3.10 - Editor: Fix 'Gizmo Lock' with rotation gizmo. Fix incorrect displaying '#n' as '\n' form lang file. Fix SaveAs without format.   
0.2.3.9 - Editor: Settings Panel + Localization: English, Russian + Basic Gizmos support + fixed #0002 bug.   
0.2.3.8 - Core: Recreate the Force Application system. Removed CoreApp, and replace by ApplicationPlatform.  
0.2.3.5 - Editor: Recreate and improve Console Log panel, fix bugs with coping/pasting unvalid game objects.   
0.2.3 - Editor: Add console log panel, when shows all major changes, and more icons. Graphics: WGL: Context now creates natively using wglCreateContextWithAttribs().   
0.2.2 - Graphics: RenderEngine2D: Add beginBatch() and beginNewBatch() functions + fix memory leak on destroying renderer.    
0.2.1 - Debug: Profiling: Fix memory leak in Instrumentator. (don't have destructor.)   
0.2.0 - Core: CTXEngine renamed to Force. Editor: Add support for saving tags per scene. Copy-Cut-Paste system, user can now copying, pasting, cutting the game objects with UI Menus and shortcuts. Window: Win32: Fix the minimum size of window.   
0.1.21.12 - Editor: Added YAML Serializing library. Now user can load and save scenes in/from .ctx format pretty easly. Also added editor icons on InpsectorPanel. Refresh desing of CTXEditor.   
0.1.21.10 - Editor: Recreate the UI for transform component, add colored XYZ reset-buttons and move the labels in to left side. Graphics: GL3: Refactoring GLIndexBufferObject, now OpenGL 3.x support 16 bit IndexBuffers.   
0.1.21.9.6 - Graphics: D3D11 & GL3: To DirectX 11 add dynamic buffer creation and data rewriting. In OpenGL 3.x add dynamic rewritting by glMap/glUnmap.   
0.1.21.9.3 - Graphics: D3D11: Fully implement D3DShader and fix memory leak. Now D3D has fully base abstraction to create basic mesh. GL: Remove 'selected' flags from VertexArray, VertexBuffer, IndexBuffer.   
0.1.21.9.2 - Graphics: D3D11: Add D3DShader, but with bug, big memory leak. Next commit shoud fix that problem.   
0.1.21.9 - Graphics: D3D11: Continue to implement Direct3D 11. Add D3DVertexArrayObject, D3DVertexBufferObject, D3DVertexIndexBuffer, update layout and format system. GL3: Add few new shader data formats.   
0.1.21.8 - Graphics: D3D11: Implementing raw DirectX 11 work pipeline. Add D3DContext, D3DGraphicsAPI, D3DHelper. Draw rect with index buffer.   
0.1.21.6.9 - Window: Win32: Fixed visibale flag, and now window can be showed or not by controlling flag. WindowPlatfrom in win32 now stores hInstance and hwndClass pointers.   
0.1.21.6.8 - Window: Win32: Fixed back (Y axis) mouse scrolling. Fix bug with cursor when updating in rect of window. Add to handle five new messages in WinProcc.   
0.1.21.6.5 - Editor: Improve editor functionality. Fully recreate desing. Add dark and white themes. RenderEngine: Add support for basic lighting. Window: Fix displaying of uncorrect title.   
0.1.21.6.4 - Editor: Add Tag Component UI, Tag list, Tag Add button, GameObject Add button.   
0.1.21.6.3 - Editor: Add Camera Properies UI Panel. And upgrade editor, fix uncurrect projection resize.   
0.1.21.6.2 - RenderEngine: Update RenderEngine 3D, add support for TextureCube, advanced Depth Testing. Editor: Inspector panel now shows currect data about GameObject's and Components.   
0.1.21.6.0 - Assimp + Editor: Add support to loading any model from modeling program, and add new Editor Panels.   
0.1.21.5.3c - Input: Recreate fully input system. Window: Add global callback system.   
0.1.21.5.2c - Window: Add global callback system, i.e Win32 and GLFW works uses CTXEngine callbacks.   
0.1.21.5.0c - ECS: Added Components, GameObject and Scene classes.   
0.1.21.4.0c - Win32 Support: Window, OpenGL context, ImGui + lazzy Input.   
0.1.21.3.12c - EnTT and Core Refactoring.   
   
From 0.1.20 to 0.1.21.3.10 (The Core Pipeline Update):   
   
0.1.20.3.10c - New Configuration System.   
0.1.20.3.9c - Element + Scene + App structure recreation and fixing Editor events.   
0.1.20.3.7c - Support More that 32 textures on Render + black rect on some devices.   
0.1.20.3.6c - Editor Viewport + Upgrade light.   
0.1.20.3.5c - Basic 2D Lighting.   
0.1.20.3.1c - Editor Space + Project.   
0.1.20.1.8c - Patricles and SubTextures support.   
0.1.20.1.6c   
0.1.20.1.5c   
0.1.20.1.1c  
   
(2019-2020) The version of the Force/Craftix then on Java before C++:   
   
0.1.19 - The Final Fixable Update (Lwjgl 3)   
0.0.19 - The Final Fixable Update (Lwjgl 2)   
0.0.18 - Multiplayer Test Update   
0.0.17 - Menu 2.0   
0.0.16 - Second Button Fixable Update   
0.0.15 - Rotateble Menu Skybox   
0.0.14 - First Button Fixable Update   
0.0.13 - Text 2.0   
0.0.12 - Audio Update  
0.0.11 - First Menu   
0.0.11be - Bogdan Edition   
   
(2018):   
   
0.0.1 - 0.0.10   
