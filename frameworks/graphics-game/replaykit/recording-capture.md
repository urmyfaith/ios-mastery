recording-capture.md


## iOS 9


* UIViewController
  * [RPPreviewViewController](https://developer.apple.com/documentation/replaykit/rppreviewviewcontroller) : [NSExtensionRequestHandling](https://developer.apple.com/reference/foundation/nsextensionrequesthandling)

* NSObjectProtocol
  * protocol [RPPreviewViewControllerDelegate](https://developer.apple.com/documentation/replaykit/rppreviewviewcontrollerdelegate)


* NSObject
  * [RPScreenRecorder](https://developer.apple.com/documentation/replaykit/rpscreenrecorder)

* NSObjectProtocol
  * protocol [RPScreenRecorderDelegate](https://developer.apple.com/reference/replaykit/rpscreenrecorderdelegate)

## RPScreenRecorder](https://developer.apple.com/documentation/replaykit/rpscreenrecorder)

class func shared() -> RPScreenRecorder

func startRecording(handler: ((Error?) -> Void)? = nil)

func stopRecording(handler: ((RPPreviewViewController?, Error?) -> Void)? = nil)

func discardRecording(handler: @escaping () -> Void)


func startCapture(handler captureHandler: ((CMSampleBuffer, RPSampleBufferType, Error?) -> Void)?,
completionHandler: ((Error?) -> Void)? = nil)


func stopCapture(handler: ((Error?) -> Void)? = nil)


* var isAvailable: Bool { get }
* var isRecording: Bool { get }
* var isMicrophoneEnabled: Bool { get set }
* var isCameraEnabled: Bool { get set } // iOS 10
* var cameraPreviewView: UIView? { get } //
* var cameraPosition: RPCameraPosition { get set } // 11
* weak var delegate: RPScreenRecorderDelegate? { get set }

### [RPSampleBufferType](https://developer.apple.com/documentation/replaykit/rpsamplebuffertype)

* case video = 1
* case audioApp = 2
* case audioMic = 3

## [RPScreenRecorderDelegate](https://developer.apple.com/reference/replaykit/rpscreenrecorderdelegate)


optional func screenRecorder(_ screenRecorder: RPScreenRecorder,
        didStopRecordingWith previewViewController: RPPreviewViewController?,
                       error: Error?)

optional func screenRecorderDidChangeAvailability(_ screenRecorder: RPScreenRecorder)


## [RPPreviewViewController](https://developer.apple.com/documentation/replaykit/rppreviewviewcontroller)

var mode: RPPreviewViewControllerMode { get set }

### [RPPreviewViewControllerMode](https://developer.apple.com/documentation/replaykit/rppreviewviewcontrollermode)

* case preview = 0
* case share = 1

weak var previewControllerDelegate: RPPreviewViewControllerDelegate? { get set }



optional func previewControllerDidFinish(_ previewController: RPPreviewViewController)

optional func previewController(_ previewController: RPPreviewViewController,
     didFinishWithActivityTypes activityTypes: Set<String>)
