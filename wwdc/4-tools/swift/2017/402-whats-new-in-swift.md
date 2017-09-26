


swift/2017/402-whats-new-in-swift.md


• Language refinements and additions
• Source compatibility
• Tools and performance
• Standard library
• Exclusive access to memory



Swift 4—Improving Cocoa Idioms
SE-0161 Smart KeyPaths: Better Key-Value Coding for Swift
SE-0166 Swift Archival & Serialization

SE-0167 Swift Encoders


## Build Improvements - Bob Wilson, Swift Performance Team


### Existential Containers

Implementation of a value of unknown type
Inline value buffer: currently three words
Large values stored on the heap
Heap allocation is slow


### Smaller Binaries



## Swift Strings
• Faster, easier character processing

Ben Cohen, Swift Standard Library Team


More Standard Library Features
SE-0104 Protocol-oriented integers
SE-0153 Dictionary & Set enhancements
SE-0163 Improved String C Interop and Transcoding
SE-0170 NSNumber bridging and Numeric types
SE-0173 Add MutableCollection.swapAt(\_:\_:)
SE-0174 Change filter to return Self for RangeReplaceableCollection



Exclusive Access to Memory
John McCall, Swift Compiler Team



Non-Exclusive Access to Memory
Hard to reason about
Creates corner cases
Performance problems for libraries Performance problems for the compiler

Run-time Enforcement
Global variables
Properties of classes
Local variables captured in escaping closures

Taking Advantage of Exclusive Access
More reliable performance Lots of optimization
In libraries
In the compiler In your code
New language opportunities https://github.com/apple/swift/blob/master/docs/OwnershipManifesto.md




## What's New in Swift (Summary)
Language refinements and additions Source compatibility
Tools and performance
Standard library
Exclusive access to memory
