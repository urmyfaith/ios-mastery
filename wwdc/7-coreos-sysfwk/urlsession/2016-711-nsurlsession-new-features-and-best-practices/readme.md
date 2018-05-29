# [2016 711 NSURLSession: New Features and Best Practices](https://developer.apple.com/videos/play/wwdc2016/711/)

4203


Evolving NSURL

Session API Security

Best practices and tips



NSURLSession Example | 900


```swift
let config = NSURLSessionConfiguration.defaultSessionConfiguration()
let session = NSURLSession(configuration: config)

let url = NSURL(string: "https://www.example.com/")!
let task = session.dataTask(with: url) { (data: NSData?, response: NSURLResponse?, error:
NSError?) in
... }
task.resume()

```


Review
Summary: Three-step process
Configuration Session
Tasks


one-session-many-tasks


HTTP/2 | 1130



HTTP/2 Protocol

* Multiplexing and concurrency
* Header compression
* Stream priorities
* Server Push (NEW)

### Demo - HTTP/2 Server Push (Andreas Garkuscha) | 1810 | p81





## Security - Never an afterthought| 3620 | p159


```
$ nscurl https://insecure.example.com/

nscurl[1234:123456] NSURLSession/NSURLConnection HTTP load failed
(kCFStreamErrorDomainSSL, -9824)

$ nscurl —-enable-rc4 https://insecure.example.com/

Enabling RC4 cipher suites
<html><body><h1>It works!</h1></body></html>

```

### App Transport Security

NSAllowsArbitraryLoadsInWebContent
NSRequiresCertificateTransparency
