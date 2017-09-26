
# [Working with Metal: Fundamentals](https://developer.apple.com/videos/play/wwdc2014/604/)



## Initialization

* Device
* CommandQueue
* Resources (Buffers and Textures)
* RenderPipelineState
* View

### Get the Device


## Drawing

* command buffer
* start a render pass
* draw
* commit the command buffer

### 1 command buffer

let buffer = queue.commandBuffer

### 2 Render Pass Configuration

[`MTLRenderPassDescriptor`](https://developer.apple.com/documentation/metal/mtlrenderpassdescriptor)

get encoder

### 3 Drawing (a Triangle)


### 4 Committing a CommandBuffer

```swift
commandBuffer.addPresent(drawable)
commandBuffer.commit()
```


## Uniform and ...


render.setVertexBuffer(uniformBuffer, offset: 0 at: 1)

### CPU and GPU Pipelining

```swift
dispatch_semaphore_create(3)


{ // Per frame
  wait(, FORVER)

  commandBuffer.addCommandHandler() {
    signal()
  }
}
```


## Metal shading language

* writing shaders in metal
* data types in metal
* shader inputs, outputs, and matching rules.



### data types


### Buffers

a pointer or a reference to a type
must be declared in an address space
* global
* constant - at the same loation ..

pass by reference

#### Global vs Constant

### Per-Vertex Inputs - Option One


### Per-Vertex Inputs - Option Two

Decouple vertex input data from type used in shader

### Per-Vertex Outputs - Option One

### Per-Vertex Outputs - Option Two

### Per-Fragment Inputs

### Per-Fragment Outputs

## Shader Signature Matching

Types match

## Math in Shaders

fast vs precise mode

Handling of NaNs is undefined in fast modes


### Metal Standard Library
