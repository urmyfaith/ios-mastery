




## Ref: [Encoding, Decoding, and Serialization](https://developer.apple.com/documentation/swift/encoding_decoding_and_serialization)

Note: Most these conceptual API are in [Swift: ](https://developer.apple.com/documentation/swift/encoding_decoding_and_serialization), while JSON and PropertyList are in [Foundation: ](https://developer.apple.com/documentation/foundation/archives_and_serialization)


## Swift Standard Library


[CodingKey](https://developer.apple.com/documentation/swift/codingkey)


x | Encoding | Decoding
--|--|--
protocol, for data| [Encodable](https://developer.apple.com/documentation/swift/encodable) | [Decodable](https://developer.apple.com/documentation/swift/decodable)
protocol, for mechanism | [Encoder](https://developer.apple.com/documentation/swift/encoder) | [Decoder](https://developer.apple.com/documentation/swift/decoder)
enum error|[EncodingError](https://developer.apple.com/documentation/swift/encodingerror) | [DecodingError](https://developer.apple.com/documentation/swift/decodingerror)


x | Encoding Containers | Decoding Containers
--|--|--
struct | [KeyedEncodingContainer](https://developer.apple.com/documentation/swift/keyedencodingcontainer) | [KeyedDecodingContainer](https://developer.apple.com/documentation/swift/keyeddecodingcontainer)
protocol | [SingleValueEncodingContainer](https://developer.apple.com/documentation/swift/singlevalueencodingcontainer) |  [SingleValueDecodingContainer](https://developer.apple.com/documentation/swift/singlevaluedecodingcontainer)
protocol| [KeyedEncodingContainerProtocol](https://developer.apple.com/documentation/swift/keyedencodingcontainerprotocol) | [KeyedDecodingContainerProtocol](https://developer.apple.com/documentation/swift/keyeddecodingcontainerprotocol)
protocol| [UnkeyedEncodingContainer](https://developer.apple.com/documentation/swift/unkeyedencodingcontainer) | [UnkeyedDecodingContainer](https://developer.apple.com/documentation/swift/unkeyeddecodingcontainer)

## Foundation

x | JSON | PropertyList
--|--|--
Encoder | [JSONEncoder](https://developer.apple.com/documentation/foundation/jsonencoder)| [PropertyListEncoder](https://developer.apple.com/documentation/foundation/propertylistencoder)
Decoder | [JSONDecoder](https://developer.apple.com/documentation/foundation/jsondecoder)| [PropertyListDecoder](https://developer.apple.com/documentation/foundation/propertylistdecoder)
PropertyListSerialization| [JSONSerialization](https://developer.apple.com/documentation/foundation/jsonserialization) iOS 5| [PropertyListSerialization](https://developer.apple.com/documentation/foundation/propertylistserialization) iOS 2


* [Encoding and Decoding Custom Types](https://developer.apple.com/documentation/foundation/archives_and_serialization/encoding_and_decoding_custom_types)


## Refers


[Ultimate Guide to JSON Parsing With Swift 4](http://benscheirman.com/2017/06/ultimate-guide-to-json-parsing-with-swift-4/)

https://medium.com/tsengineering/swift-4-0-codable-decoding-subclasses-inherited-classes-heterogeneous-arrays-ee3e180eb556
