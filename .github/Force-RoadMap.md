# Force Development Features

### Main Roadmap

| Feature           | Description                                                          | State                        |
|-------------------|--------------------------------------------------------------------  |------------------------------|
| Core              | Build basic workstation to work with Force.                          | +                            |
| Window System     | Handle windows on different platforms.                               | +                            |
| Renderer 2D       | Batch Renderer: Quads, Lines, Circles, Sprites.                      | +                            |
|                   | Font Rendering: Support for text and font.                           | Working...                   |
|                   | UI Rendering: Support for UI/GUI/HUD rendering.                      | Working...                   |
| Renderer 3D       | Basic model loading, basic shaders and renderer.                     | 2023-?                       |
| Project System    | Apportunatty to create, save, and edit projects.                     | +                            |
| Scene Managment   | ECS. Creating, saving, controlling, playing scenes.                  | +                            |
| Asset Managment   | Creating, importing, saving, display, attach to GameObjects assets.  | +                            |
| C# Scripting      | Mono and scripting projects, feature to create scripts, attatch to   |                              |
|                   | GameObjects and play.                                                | +                            |
| Physics 2D        | Box 2D physics.                                                      | +                            |
| Physics 3D        | XPhys physics.                                                       | 2024-?                       |
| Audio             | Playing effects and sounds.                                          | +                            |
| Editor Tool       | Force Editor Tool, to create projecs and games. Main focus today.    | Working...                  |
| Nave Tool         | Force Launcher allowing download, search builds, and create projects.| Working...                   |
| Runtime           | Goal to play created project outside the Editor.                     | +                            |
| Platforms         | Windows, Linux, Mac.                                                 | +--                          |
| Renderers         | OpenGL, DirectX10, DirectX11, DirectX12, Vulkan, Metal, Mantle.      | +++----                      |

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
| Folder Asset                                  | +                            |
| Image Asset                                   | +                            |
| Audio Asset                                   | +                            |
| Script Asset                                  | +                            |
| Scene Asset                                   | +                            |
| Prefab Asset                                  | +                            |
| Custom User Assets                            | -                            |