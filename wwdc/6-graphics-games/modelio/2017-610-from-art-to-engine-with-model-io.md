
# [2017 610 From Art to Engine with Model I/O](https://developer.apple.com/videos/play/wwdc2017/610/)




## USD Universal Scene Description

[Official Link](https://graphics.pixar.com/usd/docs/index.html)

### Composition

### Classes, Variations, and Overrides

### Powerful Text Format, Fast Binary


## Introducing the Pipeline

Scriptable command line tool

* Repeatable
* Consistent
* Scriptable
* Scalable
* Composable

## Baking Ops

### 1 Geometry + Transform


```swift
//for every mdlObject in MDLAsset:
if let mesh = mdlObject as? MDLMesh {   
  vertexDescriptors.append(mesh.vertexDescriptor)
  for vertexBuffer in mesh.vertexBuffers {
    let vertexBufferData = Data(bytes: vertexBuffer.map().bytes, count: vertexBuffer.length)
    ...
  }
  for submesh in mesh.submeshes! {
    if let indexBuffer = (submesh as? MDLSubmesh)?.indexBuffer {
      let indexBufferData = Data(bytes: indexBuffer.map().bytes, count: indexBuffer.length)
      ...
    }
  }
}
```

### 2 Texture Paths + Materials

```swift
// for every submesh:
if let material = submesh.material {
  for property in material.properties(with:<MDLMaterialSemantic>) {
    if property.type == .string || property.type == .URL {
      // texture
    }
    else if property.type == <MDLMaterialPropertyType> {
         // uniform value
    }
  }
}
```

### 3. Instancing Data

## Demo
• Geometry, Materials, and Instancing Nicholas Blasingame, Game Technologies Engineer


## Slide [24]

###  4. Transform Animation

### 5. Skinning + Character Animation


A | B
--|--
Mesh Data| Descriptors <br> Vertex + Index Buffers
Scene  Composition Data| Parent Indices, Mesh Indices  Instance Count
Transform Data| Local Transforms  Animated Local Transforms  Animation Clips
Material Data| Material Uniforms Texture Paths
Skinning Data| Inverse Bind Transforms Joint to Palette Mapping Skeleton Parent Indices


## Demo
• Instancing and Characters
