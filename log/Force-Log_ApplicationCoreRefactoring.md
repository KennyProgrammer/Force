# Force 0.3.9pre1

Application System and Core Refactoring:
   - Replace old Config class by new ApplicationSpecificaion. 
   - Add ApplicationCmdArgsSpecification, ApplicationWindowSpecification. Now application knows about its working path and resources directory.   
   - Add ApplicationUserSpecification instead of Project::ProjectConfig. Remove Project::ProjectConfig.   
   - Now instead ForceConfig.json Force creates ForceUser.json from ApplicationUserSpecification.   
   - Application now can runs without ImGui context and element. Add ApplicationPlatformSpecification.   
   - Refresh, redising, update, remove unnessisary code.
   - Now scripting backend initialize not by Application, by platform Entry Point. Because Mono JIT cannot be reloaded if it was CleanUp.   
   - Update the application system, add Core.h/cpp files that initialize the core systems. Improve closing via new Shutdown function. Now application update loop is updates by running flag not by window->IsCloseRequested.   
   - Now user can disable rendering and audio engines. (But it will still links and requrie DLL's.)   
   - Add ApplicationVersionFlags to decompose the compared version by Application::CompareVersion().   
   - ApplicationBootSpecification now accept list of arguments that comes from cmdlineArguments.   
   - Add SetupSpecification for Application. And connect last project and window changes, such as checking to all Window's was destroyed.   
   - Remove old OnUpdate function, devide it to BeginFrame and EndFrame, and add PresentFrame with two different modes...   

Element System Refactoring:
   - Improve the element system, add category for element and advanced callaback sending via ElementCallbackClass.   
   - Add new OnFrameOver event that need to use when need complely redraw frame in the single thread, but dynamiacally.   

