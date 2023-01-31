# Force 0.3.9pre1

Renderer Refactoring:
   - Rename BufferImpl file to BufferTypes (refactor file) 
   - Remove BufferImpl class.
   - Clean up the Attribute, BufferLayout.
   - Remove inheretece of VertexBuffer, IndexBuffer from BufferImpl.
   - Remove PutBuffer(BufferImpl) from VertexArray.
   - Remove buch of unused functions and old comments from VertexBuffer and IndexBuffers.
   - Move implemnetation of GetType() to abstract classes. (VertexBuffer, IndexBuffer).
   - Remove GetData() (VertexBuffer, IndexBuffer)
   - Remove PutData() (deprecated version), GetData() from VertexBuffer.
   - Move IndexCount, IndexCount16 to BufferTypes.h.
Renderer OpenGL:
   - Remove GetID() from VertexBuffer.
   - Remove DeleteAttribute() from VertexBuffer.
   - Add BufferUsageToOpenGL to VertexBuffer, IndexBuffer.
   - OpenGL has impementation of realocating IndexBuffers but is wrong. Force support only unmutable index buffers.
Renderer Direct 11/10:
   - Add BufferUsageToD3D/10 to VertexBuffer, IndexBuffer
