

# Numeric

## Hierarchy

* Numeric
  * SignedNumeric - CGFloat , Decimal
    * [`FloatingPoint`](https://developer.apple.com/documentation/swift/floatingpoint)
      * [`BinaryFloatingPoint`](https://developer.apple.com/documentation/swift/binaryfloatingpoint) - CGFloat, Float, Float80, Double
    * [`SignedInteger`](https://developer.apple.com/documentation/swift/signedinteger) - Int , Int8, Int16, Int32, Int64
  * [`BinaryInteger`](https://developer.apple.com/documentation/swift/binaryinteger)
    * [`UnsignedInteger`](https://developer.apple.com/documentation/swift/unsignedinteger) - UInt, UInt8, UInt16, UInt32, UInt64



## [`Numeric`](https://developer.apple.com/documentation/swift/numeric)

associatedtype Magnitude : Comparable, ExpressibleByIntegerLiteral

init?<T>(exactly source: T) where T : BinaryInteger

var magnitude: Self.Magnitude { get }

op | op | assign  | uniop
--|--|--|--
add/plus/sum| `static func +(lhs: Self, rhs: Self) -> Self` | `static func +=(lhs: inout Self, rhs: Self)` | `static func +(Self)`
minus |`static func -(Self, Self)` | `static func -=(inout Self, Self)`
multiply | `static func *(Self, Self)` | `static func *=(inout Self, Self)`


## [`SignedNumeric`](https://developer.apple.com/documentation/swift/signednumeric)

mutating func negate()

prefix static func -(operand: Self) -> Self

## [`BinaryInteger`](https://developer.apple.com/documentation/swift/binaryinteger)

associatedtype Words : Sequence where Self.Words.Element == UInt
