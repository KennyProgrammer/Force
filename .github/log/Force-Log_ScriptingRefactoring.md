# Force 0.3.9pre1

Scripting Refactoring:
	- Scripts instantiates now only in runtime. Before it was like when attach script it already instantiate it in Edit Mode.   
	- Improve Build Script Engine, now its builds on different thread and you can still working in Editor without waiting.   
	- Remove hold bunch stuff from MonoBackend, now MonoScript has its own file that has MonoScriptClass and MonoScriptInstance.   
	- Fix critical bug, that monoScripts & monoGameObjects will instaintates in editor scene, and when you copy Scene using Copy(),
its copy the address of monoScripts & monoGameObjects in to runtime scene. So when we later modify pointers to ms & mgos later
throw runtime scene, its also modify it in editor scene, because editor & runtime scenes has self the same address to  monoScripts & monoGameObjects.
So this later in runtime lead to wheird issues with physics wrong insantiation, or ever using previous script (gameobject) from last play.   
	- Rework the rebuild scripts in runtime, add new options in to Preferences -> Editor -> Rebuild Scripts In Play Mode.   
	- Devide script fields reading/writting in two behaviour states, Editor & Runtime.   
	- Implement the Rebuild And Continue Play at runtime.   
	- Total FIX: Fix a freaking hold bunch of memory leaks with mono: mono_string_new_wrapper replaced by mono_string_new. mono_string_new_wrapper actulally
 not free the string and no way to free it its just wrapper over mono.  So mono_string_new_wrapper used in Force script engine almost in each function so always before was memory leak.
	- Prefabs: Now new instantiated prefabs not copy any script component.   
	- Prefabs: With new attach prefab system, now prefabs dynamically save it Prefab UUID handle that points before reloading script and set it back in monoGameObjects & in script fields.   
	- Prefabs: After reloading script at runtime, if prefab has instantiate on true, it will be ignored for case of unnessisary duplication.   
	- Displaying and dynamic changing script fields   
	- Fix bug with deleting script component in runtime. (Any script component cannot be deleted from runtime. Technically its possible but it requres to remove script from mono script block execution and releasing 
gc handle. But eventially when we back editor mode that script will exist, because saved in editor scene. So better way just use excecute to false in script component).   
	- Now Force detect status of build script project from MSBuild, and print correspond messages.   

// Global script fixing:

	- When reloading scripts at play mode object still have old assembly pointer.  See OnStart() vs OnValidate() +
	- Fix deleting objects at runtime. +
	- Edit name in runtime not affect on instance of object in script. +  
	- Tag in runtime not affect on instance of object in script. +   
	- Transform in runtime not affect on instance of object. +   
	- Transform with physics not affect on instance of object. +   
	- Runtime fixture not became NULL on colliders when body destroy it. +   
	- Fix bug that script project include the scripts from Backup folder. For example old ExampleScript.cs.    +
	- Fix bug that script fields not appears in simulation mode. +