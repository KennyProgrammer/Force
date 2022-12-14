Status: (F) - Fixed, (A) - Active, (C) - Critical   
Type: (K) - Kernel,   
	  (I) - IO,   
	  (E) - Editor,   
	  (G) - Graphics,   
	  (W) - Window,   
	  (A) - Audio,   
	  (P) - Physics,   
	  (S) - Scene/Scripting/Project,   
	  (M) - Assets   
	  (N) - Nave   
    
(F/E) #0163: Fixed bug that when user in not scene/project state when click on play, scene not display currect message.    
(F/E) #0162: Fixed bug when rename scene, somehow gets buffers overflow when name is bigger that reuqested, for example when scene is --NotSerializebleScene--.   
(F/E) #0161: Fixed incurrect style with white theme with borders on the window.   
(F/E) #0160: Fix bug with deselecting objects when move explorer panel.   
(F/E) #0159: Fix bug with crahsing in Assets Browser when size is too small of the window on Y.   
(F/E) #0158: Fix bug with object selection when clicking on Toolbar.   
(F/E) #0157: Fix bug that audio and camera sprites process invalid selection object ID.   
(F/S) #0156: Camera Background is not serialized.   
(F/E) #0155: Glitching when selection area renders with collider's area.   
(F/P) #0154: Incorrect box collider displaying.   
(F/K) #0153: std::exception (Uncurrect user profile symbols).   
(F/E) #0152: Refer to to not working fix (#0058). Somehow fix this bug, but break ImGui because cut-out ability to render when press Ctrl+Tab. Eventity we don't need it for a Game Engine.   
(F/E) #0151: Fix bug when we exit from runtime by press Shift+Esc now blocks Shift and not let move editor camera down until we released it, and the same with project saving.   
(F/S) #0150: Fix that object was unvalid for explorer after Object.Destroy(gameObject) because selectedObject still has old game object.   
(F/E) #0149: Fix bug if selectedThumbnail not exist we cannot preview asset just deselect it and set inspector view to Empty.   
(F/S) #0148: When create new project throw Nave or Editor its not setting up the build configuration for scripts so i think its just empty string "why???" so breaks initial script compilation. Until save settings.   
(F/S) #0147: When create new project throw "Nave" its script premake5.lua file not link to Editor so breaks initial script compilation.   
(F/S) #0146: Bug with crashing Mono sometimes when reload assemblies. Most cases happens after reopen or open new project.   
(AF/S) #0145: Bug that sometimes when settings is resoring or/and reopen project and build not with Debug but Release, or someting like that pEvents and pScriptClass becomes NULLPTR.   
(F/E) #0144: Fixed crash with resizing Inspector and Assets Browser when below min clip rect size.   
(F/S) #0143: Fixed bug that script project generates uncurrect Editor paths for Premake5.   
(F/E) #0142: Fixed bug when script engine is building we cannot close/open project/scene.   
(F/A) #0141: Audio clip was not currect loaded, if .ext asset file is missing.   
(A/P) #0140B: Physics system uncurrect plays when click or press on non-client area on Win32 window. But works perfecly with move/resize.   
(F/W) #0140: Fixed very old bug since 0.1.21, to not redraw content with any GraphicsAPI on Win32 client area when move/resize messages as sended.    
(F/P) #0139: Fix bug that DestroyRigidbody2D not say colliders components that fixture was destoryed by body and not set to NULL.   
(F/S) #0138: Fix Edit name and tag in runtime not affect on instance of object in script.   
(F/E) #0137: Fix uncurrent rendering CSharpScriptComponent normaly and with different order.   
(F/E) #0136: Fix bug with uncurrect closing component list and tag manager.   
(F/S) #0135: Fix bug with deleting objects at runtime, was duplicate deletion in monoGameObjects.   
(F/E) #0134: Fix bug when close project in fullscreen mode, it already show startup page, but preload the open last saved project.   
(F/E) #0133: Fix bug when reloading application is not reset the static Inspector DrawComponentOrder.   
(F/E) #0132: Bug when object has the same ENTTID not UUID in explorer, incurrect selected flag.   
(F/E) #0131: Fixed bug during opening project assets imports after that load startup scene, or asset scene, because scene is asset and requre to loaded before.   
(F/E) #0130: Fixed completly the drag drop API for Browser and behaviour of DrawThumbnail. It includes small & critical bugs that happens when dragging asset/item.   
(F/E) #0129: Fixed start dragging. Add delta to resolution of 5px to start drag in Browser.   
(F/E) #0128: Fixed bug to not allow go back on SubBarPanel if directory tree has identical folders.   
(F/M) #0127: Fix bug with IterateOver function, if directory not exist we skip the iteration.   
(AC/IW) #0126: Bug with FE_KEY_DELETE in my Force Win32 Input Implmentation, that block input in Imgui input box and maybe something else. This bug appears only if we press to DELETE and show Win32 MessageBox. No any idea how fix this, seems throw ImGui Key Pull this works fine.   
(F/E) #0125: Fixed bug when input from Editor OnEvent blocks when focused to another panel and in SceneState::EMTPY.   
(F/E) #0124: Fixed very old bug with camera scrolling when other panel is focused.   
(F/M) #0123: Fixed bug when asset's parent path (folder) not have actuall asset file, it created new one with idefinded behvaiour Zero UID.   
(F/E) #0122: Fix bug with not update assets root directory when new project created/opened.   
(F/W) #0121: On Win32 when disable cursor its not hide the icon. Problem was with WndProc in ImGui.   
(F/G) #0120: PlatformLoader: GLFW not was create the graphics context.   
(F/I) #0119: Fix bug that Force Input not call pool events for GLFW.   
(F/K) #0118: Fixed bug with Creating 'Input' as Ref but also deleting raw pointer at initialization/deinitialization.   
(F/E) #0117: Editor Element was not clean up ShaderLibrary.   
(F/K) #0116: Element not have destructor that doesn't destroy some elements.   
(F/E) #0115: EditorElement was not freeing objects from GPU (Framebuffers, Textures).   
(F/K) #0114: Fix bug the ElementEngine never delete elements apon destruction.   
(F/K) #0113: Fix but that Application & EditorElement never free the their Instance in destructor.   
(F/K) #0112: Fix bug with crash in **PlatformUtils::ShowMessage()** when window was destroyed or not even created.   
(F/A) #0111: Refer to not working fix (#0072). Now audio files and AudioEngine should probably safe delete all resources.   
(F/G) #0110: DirectX11/10: When imgui is disabled render image in points. Maybe problem with z-depth ordering.   
(F/K) #0109: GLFW: KeyClicked not implemented in GLFW so i use the same behaviour as KeyDowns.   
(F/G) #0108: Graphics: Win32/GLFW+GL: Fixed bug that main viewport actually not swap any buffers, and i saw this only when disable ImGuiElement for runtime.   
(F/W) #0107: Win32: Default IDC_ARROW cursor was not even loaded, because cursor pointer was not set but not FE_NULLPTR.   
(C/K) #0106: Windows: Sometimes crash in nvwgf2umx.dll in release mode. Refer to https://answers.microsoft.com/en-us/windows/forum/all/game-crash-faulting-module-name-nvwgf2umxdll/5c6171b0-92df-483c-be83-86219ab8d17a   
(F/E) #0105: Fix the issue that Preferences window opens sometimes on project start.   
(F/M) #0104: Fix bug with renaming asset, remove unnessisary code when delete not folder assets.   
(F/S) #0103: Fix bugs with scene manager, replace RemoveByAddress on Unload for removing scene from memory.   
(F/S) #0102: Fixing bug that GameObjects transforms and physical data not currenlty updates to/from Mono.   
(F/S) #0101: Fixing bug that data not send to Mono after OnStart().   
(F/S) #0100: Fixing bug that GameObject that was created from script not send its components data to Force.   
(F/E) #0099: Fix bug with deleting assets, current selectable asset not update it info.   
(F/S) #0098: Fix bug with not current loading script via drag drop.   
(F/S) #0097: Fix bug with not properly saving string fields values.   
(F/S) #0096: Fix bug when call one of Find_() methods its return new instance to C# object not that witch exist in monoGameObjects, and its block opportunity to change object in script.   
(F/A) #0095: Fix issue when select audio asset in browser it load clip at same time and if file is large is not efficent, now audio clip loading on play for preview.   
(F/E) #0094: Fix bug when opened new project/scene, in runtime its not stop the scene.   
(F/S) #0093: Fix bug when opened new project, its have old ForceCS.dll from previous project.   
(F/E) #0092: Fix bug with not closing browser.   
(A/W) #0091: Fix bug with resizeble flag on Win32 does nothing.   
(F/E) #0090: Bug when Startup Scene not found in Assets leads to crash bad_allocation.   
(F/S) #0089: Fix bug with incurrent display liked asset after moving/copying item if AssetInfo still showing.   
(F/E) #0088: Fix incurrect displaying of prefab icon on Click+LMB. (Reference to #0025).   
(F/S) #0087: GameObjectComponent was not copying to runtime scene.   
(F/S) #0086: Prefab, ActiveInScene, ActiveSelf was not serialized and deserialized.   
(S/S) #0085: Sometimes reimport assets more the one time.   
(F/S) #0084: Fix issue, on import asset to not update that folder desc when in was imported.   
(A/S) #0083: Sometimes in really rare about 1% cases beginDrag == true and you cannot drag anymore.   
(F/S) #0082: Sometimes when moving assets with double folders to throw double and more dirs its duplicate folder name or pass incurrect path to lead to crash on ReadFile.   
(F/E) #0081: Fix bug with moving item to item, and folder to inself.   
(F/E) #0080: Fix issue that cannot drag scene item into viewport in state SceneState::EMPTY.   
(F/S) #0079: Bug when reimport assets or via moving from explorer or OS into top "Assets" dir its try to open its .ext file that should been exist.   
(F/S) #0078: Bug with removing complex assets (Folders that contains other folder and files).   
(F/S) #0077: Fix issue with draging from OS files not update folder asset.   
(F/S) #0076: Fixing bug with renaming and deleting assets (not modify its parent folder asset.)   
(F/E) #0075: Fix with when double click on (not selected) thumbnail it selected it but not open. (Or need was clicking really fast)   
(F/S) #0074: Asset folder not update information when move or create new asset inside it.   
(F/S) #0073: Bug with creating folders with uncurrect asset.   
(F/A) #0072: Fix bug with not closing the audio snd file.   
(F/E) #0071: Fix bug with dragging when drag state activates when thumbnail selected it start drag outside the browser window.   
(F/E) #0070: Fix bug with dragging in general, now icon of item that dragging displayed everywhere on window and not manially set to another grag item.   
(F/E) #0069: Fix bug with incurrect begin drag state. Sometimes it set begin drag on true but restoing to false, and you cannot drag anymore.   
(F/E) #0068: Is we double click on folder and opened it, we need to block preview asset to not automatically show preview of another item in folder.   
(F/E) #0067: Fix bug when creating file/folder and it state input box asset .ext file create with initial name.   
(F/K) #0066: Fix bug with not closing some of opened file streams.   
(A/E) #0065: Fix bug with deleting object that have loaded texture asset.   
(F/E) #0064: Increase perfomance of ProjectBrowser removing the slow filesystem::relative function and filesystem::directory_iterator.   
(F/E) #0063: Fix bug with dragging content items by name not filepath.   
(F/E) #0062: Bug with not displaying hithlight rect on browser viewport when dragging file from OS.   
(F/E) #0061: Bug with not displaying hithlight rect on scene viewport when dragging scene.   
(F/E) #0060: Bug with draging scene to view   
(F/E) #0059: Bug with not currect displaying buttons is none-scene view.   
(A/E) #0058: F__KING BUG (since beginning 0.1.21): FIX ANYWAY: Disable the focus to ImGui window by press ALT.   
(F/E) #0057: Bug with csharp project: on project loading if c# project files not found - regererate it.   
(F/E) #0056: Non scene is attached open additional scene, scene not displaying.   
(F/E) #0055: Fixed bug with some popups is moving by mouse, and have uncurrect theme.   
(F/E) #0054: Fixed bug when open gameobject popup is not selected object.   
(F/ES)#0053: Fixed bug when unload last scene and render 'fake' scene from EditorElement::editorScene.   
(F/E) #0052: Fixed bug when dock panels inside UIToolbar & EditorElementViewportPanel is dissapears.   
(F/E) #0051: Fixed bug with not saving previous project if it was changed when create new one.   
(F/A) #0050: Fixed bug with audio clip was not loading when scene is saved with attaching audio clip, means that audio clip already stored in audio engine.   
(F/S) #0049: Bug when renaming script file from outside of Force made it missing but dif path, when it already attached to object is crash.   
(F/A) #0048: Bug when audioclip to source is not attaching but trying to access to it.   
(F/E) #0047: Fixed bug that EditorCamera not save it state when clicking on button in UIToolbar.   
(F/S) #0046: Moved all project settings from Resources/Editor/Settings.forceset to Project Info.   
(F/E) #0045: Fixed bug when clicking on buttons in UIToolbar and select objects.
(F/G) #0044: Fixed D3DSampler::~D3DSampler() bug.   
(F/K) #0043: Fixed bug with memory corruption on EditorElement and objects around it (I Guesss).   
(F/S) #0042: Bug with not updating components data of second+ script. Now update component if one script attached.   
(F/E) #0041: Bug if object not selected and play refers as unvalid object.   
(F/E) #0040: Restore the removed feature with maximize/minimize playmode.   
(F/E) #0039: Fixed audiosources not pause playing when click on pause mode or call Pause() from script.   
(F/E) #0038: Bug if script not excecutable, excecute code from OnStart() and maybe other methods.   
(F/E) #0037: Fixed crash when try to load new project if it not found.   
(F/E) #0036: Fixed crash when not any script components will attached, but trying send data to monoGameObject that was null.   
(F/E) #0035: Fixed bug when instead of click to play button you can hold it.   
(F/E) #0034: Fixed bug when with creating file ForceConfig with newUser false. If file not exist that means we run Force first time on this User.   
(F/E) #0033: Fixed bug in Create Project Window with flags ShowMore & Only2D. Was modified the same variable.   
(F/E) #0032: Fixed print message "Doesnt have main camera.... " in Create Project View.   
(F/E) #0031: Fixed interaction with mode buttons in Create Project View.   
(F/E) #0030: When playmusic at playback and clilk play (Active) - Fixed.   
(F/K) #0029: Bug with crashing at the end (after main()) some pointers not currectly destroyed. (I think is normal for such a large project.)   
(F/W) #0028: Bug with crahsing sometimes when window class is unregistered.   
(F/W) #0027: Fix bug with fullscreen window on all avaliable platforms including Win32.   
(F/K) #0026: Fix the crash on window input when exception is thrown. Now main try-catch blocks hides the window and user cannot iteract with main window.   
(F/E) #0025: Fix the incurrect icon rendering on ExplorerPanel-RMB-Create Object.   
(F/E) #0024: Fix the ImGuizmo rotation bug with uncurrect text formating.   
(F/W) #0023: Bug with cursor clitching a the left-top corner of the window. Only Win32 in Release mode.   
(F/W) #0022: Catch up the bug when context.SwapBuffers() crashes. Its hole time was the Vector2f constructor calling in input.setMousePosiiton({x, y}), calling in Glfw/Win32_CursorPosCallback() calling in SetCursorPosCallback(). The Vector2f constructor somehow throws bug or exception on Win32 thread.    
(F/E) #0021: Fix dymanic changing theme. Some frames not changing before reloading editor.   
(F/E) #0020: Change ImGui::Text to ImGui::TextWrapped to wrap text when not enougth space on the screen.   
(F/E) #0019: Fix bug with crash on deleting elements from log panel.   
(F/G) #0018: Crasing when VertexBufferObject delete already deleted or unexisting VertexBuffer or IndexBuffer.   
(F/K) #0017: Fix nasty bug when engine crashing on window exit button or randomly when using PlatformApplication::Exit() function.   
(F/K) #0016: Fix the bug with crashing the engine on close user scrolling the mouse.   
(F/E) #0015: Bug with moving editor camera around with LMB+MouseBTN.   
(F/K) #0014B: Full recreate input system, and now its finally works as excpected.   
(F/W) #0014: Break down the input on Win32 window. Not all keys but some, and mouse scrolling doens't work.    
(F/G) #0013: Open GL3.3 dosen't render the batch textures. Its bug since begin of '2020' when im write the batch renderer, but im tested on my low loptop and remember it.   
(F/G) #0012: On old devices with OpenGL3.3 Framebuffer was black.   
(F/K) #0011: Bug with resizing id attachment in framebuffers, memory leak.   
(F/W) #0010: Fix uncorrect title when new scene is created, displayed old scene title.   
(F/E) #0009: When using 'Camera' object with Gizmos, its shift the Gizmo model itself in other game objects.   
(CFA/W) #0008: In Win32+GL created context using wglCreateContextWithFlags is creates small waves on window.   
(A/E)   #0007: Incorrent scaling of sub-windows on resize. ImGuiWindowFlags_.   
(CA/E)  #0006: When sub-window is opened it has a part of space off main window, on clicking it is dissapears. Only GLFW+ImGui. {from 0.2.3}   
(F/K) #0005: Bug with incorrent Open/Save dialogs path start point.   
(F/E) #0004: Flipped framebuffer image in ImGui::Image function.   
(F/G) #0003: GL4.0+ shader (Rectangle.glsl) texture Z-fighting. In GL3.3 and lower this bug still be exist.   
(F/E) #0002: Button SaveAs of Ctrl+S+Shift doesn't show the .force files and don't save actial file.   
(A/E) #0001: Bug with pasting game objects, sometimes cause std::bad_allocation. I think its because EnTT has strange id system.   
