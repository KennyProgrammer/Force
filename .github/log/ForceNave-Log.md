# ForceNave-Log

Each latest feature in each version reads from bottom -> top.

## Force Nave 1.0.4+
 - Nave: Make few changes in Nave.   
 
## Force Nave 1.0.4
 - Nave: Take a little break from Editor. Starting to recovering broken Nave. Add Client build mapping API.   
 - Nave: Move images, icons. fonts from NaveElement to proper module identical as for EditorElement.   
 - Nave: Add short version of new GUILibrary to Nave. Make Nave even compile again.   
 - Nave: Refact Nave structure, move element, applications to Core, create Module module the same as Panel for Editor.   
 - Nave: Increase title bar NC area and fix bug that user cannot close Nave because if overlapping NC area.   
 - Nave: Continue refactoring Nave. Refact Tabs, Settings, Builds, Docs. Add custom TitileBar. Fixed some bugs.   
 - Nave: Write new Client API, add client manager, command manager, improvie search clients, fix couple bugs and style changes.   
 - Nave: Fix bug that during loading clients and projects it duplicate it.   
 - Nave: Finish Client Page, and add FindThread to display spinner while searching.   
 - Nave: Complete Settings Tab. Add Installs and Downloads paths for future. Fixed bugs that some settings was not saved.   
 - Nave: Complte Projects Tab, add Find Threads for clients and project searching and new UI.   
 - Nave: Complete NewProjects Tab, recreate creation project system for Nave, and add new thread and new UI.   
 - Nave: Fixed bug that if Force.exe property compnay is not Kenny Company that files now is not Force applications. So versions < 0.3.9 cannot be opened by launcher.   
 - Nave: Networking: At this time fully integrade Curl library in to Force. See comments in how_to_build and premake5.lua files for details.   
 - Nave: Networking: Create API to downloading files and arhives from server.   
 - Nave: Networking: Extend Url API, add connection check and progress callback.   
 - Nave: Add way to retrive OnlineClient's from downloaded Builds.data. Add setup for downloads and installs directories.   
 - Nave: Add Download 1/2 and CheckConnection threads. Now user can download latest Force releases and they stored in donwloads directory.   
 - Nave: Force: Add libzip library for zipping and unzipping .zip arhives. To properly use it requred zlib library that will be installed along with curl via VCPKG.   
 - Nave: Utils: Add new ZipUtils that allows zip and un-zip the archive.   
 - Nave: Update GUI library.   
 - Nave: Complete full downloading and instalation Force using from cloud. Add downloading VisualStudio aswell.   
 - Nave: Improve Docs page. Now all contents from it downloading from cloud.   
 - Nave: Complete ForceNave. Not it out of pre-release state. Offical stable release is 1.0.4.   
 
## Force Nave 1.0.2
 - Nave: Now project cannot be deleted until is opened in Editor.   
 - Nave: Fix issues with older Force versions, that lead to crash.   
 - Nave: Made Nave resizeble, and not it also redraws while move/resize curreclty.   
 - Nave: Now Nave checks its resources.   
 - Nave: Fix bug that Nave create startup scene with default name.   

## Force Nave 1.0.1
 - Nave: Starting working on super simple Launcher for Force (Force Nave).   
 - Nave: Raw implement the Force Builds (Installs) property.   
 - Nave: Implement the Installs and documentation pages. Working on Projects Tab.   
 - Nave: Implement Projects Tab. Force Builds now can be opened. Improve Installs tabs.   
 - Nave: Implement Open Project/Force button and loading Force with selected project and without it.   
 - Nave: Add Tabs icons, add Create Project Tab.   
 - Nave: Add new window for creating projects and loading it from Force Editor. This UI also moved soon in Editor creation project window.   



