# Metal Notes

Random notes as I learn more about Metal.

### Initialization

##### 1. Create a Metal device
`let device = MTLCreateSystemDefaultDevice()!`
A device is the direct connection to the GPU driver and hardware; it’s the source we need to create all the other objects in Metal.

#### 2. Create a CommandQueue
`commandQueue = device.makeCommandQueue()!`
A command queue is the communication channel to the GPU.

#### 3. Create resources (buffers and textures)

#### 4. Create RenderPipeline
A `RenderPipeline` is a chain of steps that start with taking vertex data from one end and producing a rasterized image on the other end.

The pipeline consists of two elements: the descriptor which holds the shader information and the pixel format, and the state which is built from the descriptor and contains the compiled shaders.

#### 5. Create a view
Usually just use a `MTKView`. Otherwise you can use `CAMetalLayer` attached to a regular `UIView`.
