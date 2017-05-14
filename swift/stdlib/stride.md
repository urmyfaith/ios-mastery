
[GitHub](https://github.com/apple/swift/blob/master/stdlib/public/core/Stride.swift.gyb)


Strideable [SwiftDoc](http://swiftdoc.org/v3.1/protocol/Strideable/)

func stride<T>(from start: T, through end: T, by stride: T.Stride) -> StrideThrough<T> where T : Strideable

func stride<T>(from start: T, through end: T, by stride: T.Stride) -> StrideThrough<T> where T : Strideable


func stride<T where T : Strideable>(from: T, to: T, by: T.Stride)

func stride<T where T : Strideable>(from: T, through: T, by: T.Stride)

stride | iterator
--|--
StrideThrough|StrideThroughIterator
StrideTo|StrideToIterator


## Operators

func <<T>(x: T, y: T) -> Bool where T : Strideable
