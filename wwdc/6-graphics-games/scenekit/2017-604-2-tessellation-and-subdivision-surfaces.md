## [Tessellation and Subdivision Surfaces](2017-604-2-tessellation-and-subdivision-surfaces.md)




* How . works
* New Tessellation-based geometry APIs
* Subdivision Surfaces


### Motivation

* Asset comes as a low-resolution model (coarse mesh)
* Decreased memory bandwidth
* High resolution model generated from the coarser model
  * High resolution model not stored in memory
  * Generated on-the-fly by the GPU
  * Control over the amount of detail generated


## New Tessellation-based geometry APIs

### Shader Modifiers

### Geometry Smoothing

### Displacement Mapping and

Height Map


Vector Displacement maps



### Subdivision Surfaces


### Feature-adaptive and uniform subdivision


```swift
//Subdivision Surfaces
//Adaptive subdivision on the GPU

// Enable subdivision surfaces
geometry. subdivisionLevel = 1
geometry.wantsAdaptiveSubdivision = true

// Enable tessellation
let tessellator = SCNGeometryTessellator()
geometry.tessellator = tessellator
```

<!-- ### Subdivision Surfaces -->

### Faster skinning and morphing (30)

Only the coarse mesh is animated
Leverages the GPU for morphing, skinning and refinement


```swift
//Subdivision Surfaces
//Asset authoring
// Preserve topology when importing from files
let scene = try! SCNScene(url: url, options: [.preserveOriginalTopology: true])

// Use quads when creating geometries programmatically

let element = SCNGeometryElement(data: elementData,
  primitiveType: .polygon,
  primitiveCount: 1,
  bytesPerIndex: MemoryLayout<UInt8>.size)

```


### Demo - Pottry

Use normal map to add details.

edit geometry
