network-statistics.md

## NSURLSession API [Network Statistics](network-statistics.md)| 23:50  | p91

NSURLSessionTaskDelegate new method




NSURLSessionTaskMetrics

[`URLSessionTaskMetrics`](https://developer.apple.com/documentation/foundation/urlsessiontaskmetrics) |  [`URLSessionTaskDelegate`](https://developer.apple.com/documentation/foundation/urlsessiontaskdelegate) | `urlSession(_:task:didFinishCollecting:)`




NSURLSessionTaskTransactionMetrics

[`URLSessionTaskTransactionMetrics`](https://developer.apple.com/documentation/foundation/urlsessiontasktransactionmetrics)



### Four Categories of Metrics


1 - Request and Response

* request: NSURLRequest
* response: NSURLResponse?

2 - Protocol and Connection

* networkProtocolName: String?
* isProxyConnection: Bool
* isReusedConnection: Bool


3 - Load Info

* resourceFetchType: NSURLSessionTaskMetricsResourceFetchType

4 - Connection Establishment and Transmission


###

```swift
func urlSession(_ session: URLSession, task: URLSessionTask, didFinishCollecting metrics: URLSessionTaskMetrics) {

    print(metrics)
}
```
