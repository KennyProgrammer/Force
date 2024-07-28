# Force Development Features

### Main Roadmap

| Feature           | Description                                                          | State                        |
|-------------------|--------------------------------------------------------------------  |------------------------------|
| Core              | Build basic workstation to work with Force.                          | +                            |
| Window System     | Handle windows on different platforms.                               | +                            |
| Renderer 2D       | Batch Renderer: Quads, Lines, Circles, Sprites.                      | +                            |
|                   | Font Rendering: Support for text and font.                           | +                            |
|                   | UI Rendering: Support for UI/GUI/HUD rendering.                      | Working... (20%)             |
| Renderer 3D       | Basic model loading, basic shaders and renderer.                     | 2025?                        |
| Project Managment | Apportunatty to create, save, and edit projects.                     | +                            |
| Scene Managment   | ECS. Creating, saving, controlling, playing scenes.                  | +                            |
| Asset Managment   | Creating, importing, saving, display, attach to GameObjects assets.  | +                            |
| C# Scripting      | Mono and scripting projects, feature to create scripts, attatch to   |                              |
|                   | GameObjects and play.                                                | +                            |
| Physics 2D        | Box 2D physics.                                                      | +                            |
| Physics 3D        | XPhys physics.                                                       | 2025-LQ-?                    |
| Audio             | Playing effects and sounds.                                          | +                            |
| Networking        | Internet connection and files downloading.                           | +                            |
| Editor Tool       | Force Editor Tool, to create projecs and games. Main focus today.    | Infinity...                  |
| Nave Tool         | Force Launcher allowing download, search builds, and create projects.| +                            |
| Runtime           | Goal to play created project outside the Editor.                     | +                            |
| Platforms         | Windows, Linux, Mac, GLFW                                            | +--+                         |
| Renderers         | OpenGL, DirectX10, DirectX11, DirectX12, Vulkan, Metal, Mantle.      | +++----                      |

### Core

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Core Module                                   | +                            |
| Application System                            | + (will be evolving)         |
| Element System                                | +                            |
| Exception Handeling                           | +                            |
| Memory Managment                              | +                            |
| Hooks, Modules, Players, etc...               | +                            |


### Project Managment

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Creating projects                             | +                            |
| Creating projects via Russian symbols         | +-                           |
| Serialization projects                        | +                            |
| Renaming projects                             | +                            |
| Creating projects using Nave                  | +                            |
| Handle errors during loading projects         | +                            |

### Scene Managment

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Creating scenes                               | +                            |
| Serialization scenes                          | +                            |
| Renaming scenes                               | +                            |
| Handle errors during scene loading            | +                            |
| Entity Component System                       | +                            |
| Playable and Editables scenes                 | +                            |
| Components                                    | 21 of N                      |
| Game Objects (accessors, A/T)                 | +                            |
| Prefabs, Presets                              | +                            |
| Scene Renderer                                | + (will be evolving)         |
| Physics 2D                                    | +                            |

### Scripting

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Basing Mono integration                       | +                            |
| Autogeneration C# project                     | +                            |
| Attaching & Detaching scripts throw Editor    | +                            |
| Parsing C# exception to Editor Console        | +                            |
| Debug & Logger                                | +                            |
| IO                                            | +                            |
| Rendering (Only 2D)                           | +                            |
| ImGui support                                 | +                            |
| Interaction with GameObjects                  | +                            |
| Interaction with Components                   | +                            |
| Interaction with Scenes                       | +                            |
| Runtime recompilation Assemblies/Scripts      | +                            |

### Asset Managment

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Creating & Reading Assets                     | +                            |
| Releationship beetwen .ext file and UID       | +                            |
| Reimporting assets                            | +                            |
| Deleting assets                               | +                            |
| Renaming assets                               | +                            |
| Copying assets                                | +                            |
| Importers API                                 | +                            |
| Folder Asset                                  | +                            |
| Image Asset                                   | +                            |
| Audio Asset                                   | +                            |
| Script Asset                                  | +                            |
| Scene Asset                                   | +                            |
| Prefab Asset                                  | +                            |
| Custom User Assets                            | -                            |

### Audio

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Basic Audio                                   | +                            |
| Streaming Audio                               | +-                           |

### Networking

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Writing and reading packets                   | +                            |
| Downloading files/archives                    | +                            |

### Runtime

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| Playable runtime                              | +                            |
| Exporting project to Game (via Solution)      | +                            |
| Exporting project to Game (via Editor)        | -                            |

### The Editor

| Description                                   | State                        |
| ----------------------------------------------| -----------------------------|
| There's too much to do, too big a list,       |                              |
| see Force-Log.md and logs for more details.   |                              |
| Bascially i define editor by: Editor during   |                              |
| 2D era of Force, that has a limited ending    |                              |
| and some 'competeness' of engine, and another |                              |
| 3D era of Force witch is basically infinity   |                              |
| because for 3D we can impement infinity       |                              |
| amout of features.                            |                              |


### Renderer

|                     | API                      | OpenGL 3/4    | DirectX 10/11 | DirectX 12 | Vulkan |
| ------------------- | ------------------------ | ------------- | ------------- | ---------- | ------ |
| **Implementations** | Context/Init             | +             | +             | +          | +      |
|                     | Abstract Render Commands | +             | +             |            |        |
|                     | ImGui                    | +             | +             |            |        |
|                     | Vertex Array             | +             | Using VBO     |            |        |
|                     | Vertex Buffer            | +             | +             |            |        |
|                     | Index Buffer             | +             | +             |            |        |
|                     | Uniform/Constant Buffer  | +             | +             |            |        |
|                     | Shaders                  | +             | +             |            |        |
|                     | Texture2D                | +             | +             |            |        |
|                     | Texture3D                | 3D            | 3D            |            |        |
|                     | TextureCube              | 3D            | 3D            |            |        |
|                     | Framebuffer              | +             | +             |            |        |
|                     | Adapter                  | Using Context | +             |            |        |

### Platform


|                     | OS/Platform              | Windows       |      Mac      |   Linux    |    GLFW     |
| ------------------- | ------------------------ | ------------- | ------------- | ---------- | ----------  |
| **Implementations** | Window                   | +             | -             | -          | +           |
|                     | Timer                    | +             | -             | -          | +           |
|                     | NotifyClient             | +             | -             | -          | NA          |
|                     | FileSystem (std::fs)     | +             | +             | +          | +           |
|                     | FileSystem Observer      | +             | -             | +          | NA          |
|                     | Drag & Drop              | +             | -             | -          | NA          |
|                     | Console/Terminal         | +             | -             | -          | NA          |
|                     | Platform Utils           | +             | -             | -          | NA          |