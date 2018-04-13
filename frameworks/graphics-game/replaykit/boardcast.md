boardcast.md

##






## iOS 10


[RPBroadcastController](https://developer.apple.com/reference/replaykit/rpbroadcastcontroller)

[RPBroadcastControllerDelegate](https://developer.apple.com/reference/replaykit/rpbroadcastcontrollerdelegate)



[RPBroadcastActivityViewController](https://developer.apple.com/reference/replaykit/rpbroadcastactivityviewcontroller)

[RPBroadcastActivityViewControllerDelegate](https://developer.apple.com/reference/replaykit/rpbroadcastactivityviewcontrollerdelegate)



[RPBroadcastConfiguration](https://developer.apple.com/reference/replaykit/rpbroadcastconfiguration)



## iOS 10



* NSObject
  * [RPBroadcastHandler](https://developer.apple.com/reference/replaykit/rpbroadcasthandler) : [NSExtensionRequestHandling](https://developer.apple.com/reference/foundation/nsextensionrequesthandling)
    * [RPBroadcastMP4ClipHandler](https://developer.apple.com/reference/replaykit/rpbroadcastmp4cliphandler)
    * [RPBroadcastSampleHandler](https://developer.apple.com/reference/replaykit/rpbroadcastsamplehandler)



func completeRequest(withBroadcast broadcastURL: URL,
    broadcastConfiguration: RPBroadcastConfiguration,
               setupInfo: [String : NSCoding & NSObjectProtocol]?)

func loadBroadcastingApplicationInfo(completion handler: @escaping (String, String, UIImage?) -> Void)
