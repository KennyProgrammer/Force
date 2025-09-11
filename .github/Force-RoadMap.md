# Force Development Features

### Main Roadmap

| Feature           | Description                                                                              | State                        |
|-------------------|----------------------------------------------------------------------------------------- |------------------------------|
| Core              | Build basic workstation to work with Force.                                              | +                            |
| Window System     | Handle windows on different platforms.                                                   | +                            |
| Renderer 2D       | Batch Renderer: Quads, Lines, Circles, Sprites.                                          | +                            |
|                   | Font Rendering: Support for text and font.                                               | +                            |
|                   | UI Rendering: Support for UI/GUI/HUD rendering.                                          | Working... (20%)             |
| Renderer 3D       | Basic model loading, basic shaders and renderer.                                         | 2026?                        |
| Project Managment | Apportunatty to create, save, and edit projects.                                         | +                            |
| Scene Managment   | ECS. Creating, saving, controlling, playing scenes.                                      | +                            |
| Asset Managment   | Creating, importing, saving, display, attach to GameObjects assets.                      | +                            |
| C# Scripting      | Mono and scripting projects, feature to create scripts, attatch to GameObjects and play. | +                            |
| Physics 2D        | Box 2D physics.                                                                          | +                            |
| Physics 3D        | XPhys physics.                                                                           | 2026-LQ-?                    |
| Audio             | Playing effects and sounds.                                                              | +                            |
| Networking        | Internet connection and files downloading.                                               | +                            |
| Editor Tool       | Force Editor Tool, to create projecs and games. Main focus today.                        | Infinity...                  |
| Nave Tool         | Force Launcher allowing download, search builds, and create projects.                    |                    +         |
| Runtime           | Goal to play created project outside the Editor.                                         | +                            |
| Platforms         | Windows, Linux, Mac, GLFW                                                                | +--+                         |
| Renderers         | OpenGL, DirectX10, DirectX11, DirectX12, Vulkan, Metal, Mantle.                          | +++----                      |

### Renderer

|                     | API                      | OpenGL 3/4    | Microsoft DirectX 10/11 | Microsoft DirectX 12 | Vulkan |
| ------------------- | ------------------------ | ------------- | ------------- | ---------- | ------ |
| **Implementations** | Context/Init             | +             | +             | +          | +      |
|                     | Abstract Render Commands | +             | +             |            |        |
|                     | ImGui                    | +             | +             |            |        |
|                     | Vertex Buffer            | + hidden VAO  | +             |            |        |
|                     | Index Buffer             | +             | +             |            |        |
|                     | Uniform/Constant Buffer  | +             | +             |            |        |
|                     | Shaders                  | +             | +             |            |        |
|                     | Texture2D                | +             | +             |            |        |
|                     | Texture3D                | 3D            | 3D            |            |        |
|                     | TextureCube              | 3D            | 3D            |            |        |
|                     | Framebuffer              | +             | +             |            |        |
|                     | Adapter                  | Using Context | +             |            |        |

### Platform


|                     |       OS/Platform        |     Microsoft Windows ~*7*~/10/11   |          Mac OS        |   Linux    |    GLFW     |
| ------------------- | ------------------------ | ---------------------------- | ---------------------- | ---------- | ----------  |
| **Implementations** | Window                   | +                            | -                      | -          | +           |
|                     | Timer                    | +                            | -                      | -          | +           |
|                     | NotifyClient             | +                            | -                      | -          | NA          |
|                     | FileSystem (std::fs)     | +                            | +                      | +          | +           |
|                     | FileSystem Observer      | +                            | -                      | +          | NA          |
|                     | Drag & Drop              | +                            | -                      | -          | NA          |
|                     | Console/Terminal         | +                            | -                      | -          | NA          |
|                     | Platform Utils           | +                            | -                      | -          | NA          |


### Core
- [x] Core Module
- [x] Application System (will be evolving) 
- [x] Element System
- [x] Exception And Error Handling
- [x] Memory Managment and Custom Allocators
- [x] Hooks, Modules, Players, etc...

### Project Managment
- [x] Creating projects
- [x] Creating projects via Unicode 
- [x] Serialization/Deserialization projects
- [x] Renaming projects
- [x] Creating projects using Nave 
- [x] Handle errors during loading projects

### Scene Managment
- [x] Creating scenes
- [x] Serialization/Deserialization scenes
- [x] Renaming scenes  
- [x] Components (21 of N)
- [x] Game Objects
- [x] Prefabs, Presets
- [x] Scene Renderer (will be evolving)
- [x] Physics 2D  

### Scripting
- [x] Basing Mono integration
- [x] Autogeneration C# project
- [x] Serialization/Deserialization projects
- [x] Attaching & Detaching scripts throw Editor 
- [x] Parsing C# exception to Editor Console 
- [x] Debug & Loggers
- [x] IO
- [x] Rendering (Only 2D)
- [x] ImGui (GUILibrary) support
- [x] Interaction with GameObjects
- [x] Interaction with Components
- [x] Interaction with Scenes
- [x] Runtime recompilation Assemblies/Scripts
- [x] Force.CSharp.Core classes (95 of N) 

### Asset Managment
- [x] Creating & Reading Assets
- [x] Releationship beetwen .ext (Metadata) file and Handle
- [x] Reimporting assets
- [x] Deleting assets 
- [x] Renaming assets 
- [x] Copying assets
- [x] Importers API
- [x] Folder Asset
- [x] Image Asset
- [x] Audio Asset
- [x] Script Asset
- [x] Scene Asset
- [x] Prefab Asset 
- [x] Text Asset
- [ ] Custom User Assets

### Audio
- [x] Basic Audio (.wav, .ogg, .mp3, .flac,  etc) 
- [x] Buffered Audio
- [x] Streaming Audio
- [x] Caching Audio

### Networking
- [x] Writing and reading packets
- [x] Downloading files/archives

### Runtime
- [x] Playable runtim
- [x] Exporting project to Game (via Solution)
- [ ] Exporting project to Game (via Editor) 2025bx+

### The Editor

There's too much to do, too big a list, see [Force-Log.md](https://github.com/KennyProgrammer/Force/blob/main/.github/log/Force-Log.md) and logs or more details. Bascially i define editor by: Editor during 2D era of Force, that has a limited ending and some 'competeness' of engine, and another 3D era of Force that is basically infinity because for 3D we can implement infinity amout of features.                                                          
