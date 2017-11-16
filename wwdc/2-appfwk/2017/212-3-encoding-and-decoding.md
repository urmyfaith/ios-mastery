# [Encoding and Decoding - Tony Parker & Itai Ferber, Foundation](212-3-encoding-and-decoding.m) (23.5~)

```swift
let jsonData = """
{
  "name": "Monalisa Octocat",
  "email": "support@github.com",
  "date": "2011-04-14T16:00:49Z"
}
""".data(using: .utf8)!
struct Author : Codable {
    let name: String
    let email: String
    let date: Date
}
let decoder = JSONDecoder()
decoder.dateDecodingStrategy = .iso8601
let author = try decoder.decode(Author.self, from: jsonData)

author.name
author.date



```


#### customize name

enum CodingKeys : string, CodingKey

case commitX = "commit_x"



### Demo - Itai Ferber, Foundation 30.5




### Ref: [Encoding, Decoding, and Serialization](https://developer.apple.com/documentation/swift/encoding_decoding_and_serialization)


[CodingKey](https://developer.apple.com/documentation/swift/codingkey)


x | Encoding | Decoding
--|--|--
protocol | [Encodable](https://developer.apple.com/documentation/swift/encodable) | [Decodable](https://developer.apple.com/documentation/swift/decodable)
protocol | [Encoder](https://developer.apple.com/documentation/swift/encoder) | [Decoder](https://developer.apple.com/documentation/swift/decoder)
enum error|[EncodingError](https://developer.apple.com/documentation/swift/encodingerror) | [DecodingError](https://developer.apple.com/documentation/swift/decodingerror)


x | Encoding Containers | Decoding Containers
--|--|--
struct | [KeyedEncodingContainer](https://developer.apple.com/documentation/swift/keyedencodingcontainer) | [KeyedDecodingContainer](https://developer.apple.com/documentation/swift/keyeddecodingcontainer)
protocol | [SingleValueEncodingContainer](https://developer.apple.com/documentation/swift/singlevalueencodingcontainer) |  [SingleValueDecodingContainer](https://developer.apple.com/documentation/swift/singlevaluedecodingcontainer)
protocol| [KeyedEncodingContainerProtocol](https://developer.apple.com/documentation/swift/keyedencodingcontainerprotocol) | [KeyedDecodingContainerProtocol](https://developer.apple.com/documentation/swift/keyeddecodingcontainerprotocol)
protocol| [UnkeyedEncodingContainer](https://developer.apple.com/documentation/swift/unkeyedencodingcontainer) | [UnkeyedDecodingContainer](https://developer.apple.com/documentation/swift/unkeyeddecodingcontainer)
