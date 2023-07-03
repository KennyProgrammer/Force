# Force-Bugs

Status: (F) - Fixed, (A) - Active, (C) - Critical   
Type: (K) - Kernel/Core,   
	  (I) - IO,   
	  (E) - Editor,   
	  (G) - Graphics/Platform,   
	  (W) - Window,   
	  (A) - Audio,   
	  (P) - Physics,   
	  (S) - Scene/Scripting/Project,   
	  (M) - Assets   
	  (N) - Nave   
	  
(F/E) #0262: Fixed bug that lead to crash just crash...   
(F/E) #0261: Fixed bug with incurrent selected group of assets via Shift.   
(F/G) #0260: Fixed bug that in runtime drag-drop was disabled.   
(F/E) #0259: Fix toons of final bugs with browser, espesially with dragging.    
(F/GE) #0258: Fixed bug that block drag when mouse outside window + create new one (lose focus) and popup dissapears.   
(F/K) #0257: Fixed bug that from Application ImGui Popups closed, it should be here.   
(F/G) #0256: Fixed bug that drag drop was not initialized because of Co and Ole differ threading model.   
(F/G) #0255: Win32: Fix bugs with initializing COM library.   
(F/K) #0254: Fix bug that in Debug build Scripting Backend was not be intialized because of missing left brachet.   
(F/E) #0253: Fixed bug that when tooltip or popup opens in dialog outside main window it lose focus.   
(F/G) #0252: Fix bug that CreateFile still use A instead W version to lead to crash.   
(F/E) #0251: Fixed bug with hovering toolbars and window is lose focus and glitch the new UI thin-border.   
(F/E) #0250: Fix couble bugs with go to play/simulate mode and implement auto selection for multiple objects.   
(F/E) #0249: Fix couble bugs with selection, deselection, cutting, pasting objects.   
(F/E) #0248: Fix bug that cause glitch when focus to main window from dialog, or custom ImGui parent window.   
(F/E) #0247: Fix tooltip can be shows from panel when dialog opened, and fixed some colors.   
(F/E) #0246: Fixed bug that gizmos renders on top of preview and UIToolbar buttons, and ability to use gizmos when click on them.   
(F/K) #0245: Fix bug when during shutdown if scene modified it not allowed to return to editor and menu bar renders weird during message box.   
(F/E) #0244: Fixed wrong thing, when select asset it deselect game object.   
(F/E) #0243: Fix bug that elements in datbase and global search can be activated by Enter even if its panel not hovered.   
(F/E) #0242: Fix incurrect recent projects.   
(F/E) #0241: Fix bug that panel states was not reset if panel is hidden so lead to variaous bugs.   
(F/E) #0240: Fix bug when setting Open Last Project, it was fails.   
(F/E) #0239: Fix bug with uncurrect Edit Layout.   
(F/EG) #0238: Fix bug that when draggind panel outside main window it stops to react on drag drop of windows or was glitched.   
(F/E) #0237: Fix bug when panel is platform window i cannot be dragged.   
(F/G) #0236: Sometimes then focus to main window from progress window its crashes in ntdll, or TextInputFramework.   
(F/E) #0235: Fix a litter bug when drag panel resize border and use mouse it rotate and resize window.   
(F/E) #0234: Fixed bug with lost focus to main window when progerss dialog is finished, and fix icon diplaying in status bar or error status.   
(F/E) #0233: Fix bugs with creating folder and renaming assets, asset either not created or not refresh.   
(F/W) #0232: Fix bug when restore from taskbar in not currectly fit the monitor, fix the exiting from fullscreen.   
(A/S) #0231: Bug with clicking on Skip in AssetsImporter. Sometimes   
(A/A) #0230: Crash with loading some .wav files in sndfile.c int free(psf->container_data).   
(F/G) #0229: Fixed bug that dark theme for title bar on dialog windows not working.   
(F/E) #0228: Fixed when project opened but no scene is loaded on play is not print corresponend message.   
(F/K) #0227: Bug when application is minimized CPU usage rises to about 50% of time.   
(F/G) #0226 (CRITICAL): Crash sometimes in Invalidate Scene Framebuffer in CreateTexture on D3D11/10, when resizng happens too quick.   
(F/E) #0225: Finally fixed bug with Inspector cannot be closed.   
(F/E) #0224: Bug with Cut, then Copy it removes object.   
(F/E) #0223: Fixed bug that in play mode in explorer we cannot deselect object.   
(F/E) #0222: Fixed bug that explorer uncurrect display second node of next scene. Bacause of BeginChild before DrawGameObjectNode.   
(A/E) #0221: (HARD) Bug when drag from explorer then click on ESC, or ALT, and in state mouse down hover again to that game object node it start drag it again, but it shouldnt.   
(F/E) #0220: Fixed bug when drag and press ESC and drag and use nav keys it was released mouse state.   
(F/G) #0219: GL4: Fixed bug with recompilation shader, if shader was recompiled it was not deleting prev shader id.   
(F/M) #0218: Fix bug when asset physical file was deleted but .ext file exist.   
(F/M) #0217: Fix bug when asset was deleted but some of component points to it (now its just engine start to lagging because it try to find asset AssetManaget::GetAssetByUID() every frame.)   
(F/E) #0216: Fix incurrent selecting in browser during dragging to folders, now all drop targets displays with rect and also in hierarchy.   
(F/E) #0215: Hierachy in browser was incurrent disaplying folders with flag Leaf.   
(F/E) #0214: Rename scene asset was not renamed its scene name in YAML.   
(F/G) #0213B: Create and rename files in unicode. (Only scripts cannot has a unicode name because name it actuall class name).   
(F/G) #0213: If path or file is unicode Window does not open it in explorer. (FE_PlatformUtils_OpenFile platfrom macro fix this).   
(F/E) #0212: When click on play or simulate in non project state it crash.   
(F/E) #0211: Explorer context popup is not opening with LMB in Explorer. 
(AFF/E) #0210: Audio is not hearing. (On 0.3.10 its works fine)   
(F/M) #0209: When create new project with new scene asset handle we need assign in to project.   
(F/E) #0208: Fixed bug when user open project, editor camera project was not updated from project settings.   
(F/E) #0207: Bug that when hover on SceneGame size button and click it select object.   
(F/E) #0206: Bug that in play mode we cannot drag assets via hierachy and we drag to folders it not hovered.   
(F/E) #0205: Fixed bug when game object node is selected, then hover over another game object node and try dragging its drag hovered node, now its do nothing only selected and hovered node with the same node id can be dragged.   
(F/M) #0204: Asset folder in Assets root not selected and not deleting. When reimport all assets it brokes this folder. Before ReadExt it modifiy asset .ext and set category and type None, maybe its parent folder updates of file asset and do that.   
(F/E) #0203: Scene for some reason when modified not show message when engine close.   
(F/E) #0202: When audio reloads we need to save selected UUID of object on main scene and when scene another main is loading we search the game object and make it selected in explorer and inspector.   
(F/S) #0201: Fixed bug that browser size and layout not saved properly.   
(F/E) #0200: Fixed bug when drag and press ALT it at the same time rotate scene viewport camera.   
(F/E) #0199: Fixed bug with SceneGameView toolbar buttons, it press state actives on down not click state.   
(F/G) #0198: Fix bug that Windows OpenFileBox and SaveFileBox now use UTF-16 versions to Windows can translate to Path unicode letters.   
(F/G) #0197: Fix bug that image asset witch contains russian letters it crashes.   
(F/A) #0196: Fixed bug when audio asset creates, load sound with russian letters it crashes.   
(F/E) #0195: Fixed bug with incurrect browser drop highlight rendering.   
(F/E) #0194: While dragging game object node, then hover browser, then hover other panel it not reset ImGui mouse down state to one if we still dragging.   
(F/E) #0193: While dragging preset on header of component tree is show highlight in incurrent place.   
(F/E) #0192: Fixed DragDropPresetOnBlankComponentListSpace highlight in runtime. (appears only in edit mode).
(F/E) #0191: Fixed bug that drag game object node, move out explorer and then in, it deselected currecly selected object.
(F/E) #0190: Bug when drag game object node to browser, hover browser then hover explorer it set state of explorer drag to false.   
(F/E) #0189: Bug when start drag from browser but then while dragging hover explorer game object node, Force thinks that we start drag object from explorer to browser and highlight it.   
(F/E) #0188: In runtime and simulation when drag DragDropPresetOnGameObjectNode in shows highlight rect.   
(F/E) #0187: Fixed bug when drag preset in play or simulation but it adds to edit scene.   
(F/E) #0186: Bug when exit from runtime in maximized & paused mode, its not reset panels back.   
(F/M) #0185: Asset preset incurrent recreates with incorrect type during importing.   
(F/E) #0184: Fixed unnoying and unfixeble bug that sometimes when select items it browser or then go to inspector or asset preview it randomly scrolls content of browser.   
(F/E) #0183: Fix but that DialogOpenScene when project has identical scenes with same name it select all of them.   
(A/G) #0182: WGL: Fullscreen mode is does't work, just shows black empty window even not make it fullscreen.   
(F/G) #0181: GL: Fixed bug when use logo screen window it RenderCmd or its active context points already destroyes context and upload data to VertexBuffer and get crash.   
(F/G) #0180: WGL: Fixed bug that sometimes dummy context creation fails. Incurrect PFD was set. (old bug from 0.2.0).   
(F/G) #0179: Fix bug with trying create texture with DX11/DX10 that requre (24-bit/RGB format) but Force always use RGBA (32-bit).   
(F/E) #0178: Fix bug that while rename script asset not rename script class name.   
(F/E) #0177: Fix bug when focused viewport and hovered panel that has scrollable area, when scroll it zoom-in-out camera and panel content.   
(F/E) #0176: Fix bug that in release build cannot retrive address of &EditorElement::GetPanel().GetSelectedObject(), need made a copy and then &, so not excecuting code with selection of game objects.   
(F/A) #0175: Fix big that not allow to select asset when asset deselects by Explorer.   
(F/A) #0174: Fixed big when reimporing already preview selected asset.   
(F/E) #0173: Fixed bug when drag asset user can scroll content with zooming camera.   
(F/E) #0172: Fixed reimport single asset sometimes cause to reimport all assets again.   
(F/E) #0171: Fixed the Rect tool snapping.   
(F/E) #0170: Fixed bugs with dialogs that still not open right project or delete all scenes when open new scene.   
(F/K) #0169: Fixed crash that causing when user clicked on cross window button, ImGui throws incurrect assets of missing completition frame.   
(F/W) #0168: Win32: Fixed bug with incurrent return values from WM_CLOSE message, before 'break' lead to immideatly destroying window by OS not by our call DestroyWindow.   
(F/E) #0167: Bug with duplicate projects paths points to the same project, in project startup page in recent projects.   
(F/E) #0166: Bug with large text rendering in script preview or asset script preivew - text not all text renders and window is not responce on inputs.   
(F/E) #0165: Fixed bug when scene asset preview not displays in play mode or no-scenes mode.   
(F/M) #0164: Fixed bug that assets with first attempt to reimport assets. It is not reimported.   
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
(F/W) #0091: Fix bug with resizeble flag on Win32 does nothing.   
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
(F/E) #0065: Fix bug with deleting object that have loaded texture asset.   
(F/E) #0064: Increase perfomance of ProjectBrowser removing the slow filesystem::relative function and filesystem::directory_iterator.   
(F/E) #0063: Fix bug with dragging content items by name not filepath.   
(F/E) #0062: Bug with not displaying hithlight rect on browser viewport when dragging file from OS.   
(F/E) #0061: Bug with not displaying hithlight rect on scene viewport when dragging scene.   
(F/E) #0060: Bug with draging scene to view   
(F/E) #0059: Bug with not currect displaying buttons is none-scene view.   
(AF/E) #0058: F__KING BUG (since beginning 0.1.21): FIX ANYWAY: Disable the focus to ImGui window by press ALT.   
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
(CFA/W) #0008: In Win32+GL created context using wglCreateContextWithFlags is creates small waves on window. (NOTE: 22.01.23 - Probably gone or was uncurrect VSync.)   
(F/E)   #0007: Incorrent scaling of sub-windows on resize. ImGuiWindowFlags_.   
(CAF/E)  #0006: When sub-window is opened it has a part of space off main window, on clicking it is dissapears. Only GLFW+ImGui. {from 0.2.3}   
(F/K) #0005: Bug with incorrent Open/Save dialogs path start point.   
(F/E) #0004: Flipped framebuffer image in ImGui::Image function.   
(F/G) #0003: GL4.0+ shader (Rectangle.glsl) texture Z-fighting. In GL3.3 and lower this bug still be exist.   
(F/E) #0002: Button SaveAs of Ctrl+S+Shift doesn't show the .force files and don't save actial file.   
(F/E) #0001: Bug with pasting game objects, sometimes cause std::bad_allocation. I think its because EnTT has strange id system.   
