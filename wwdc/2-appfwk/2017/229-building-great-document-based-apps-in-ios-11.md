
# [229 Building Great Document-based Apps in iOS 11](https://developer.apple.com/videos/play/wwdc2017/229/)


## New File App

File Provider

* iCloud Drive
* On my iPad/iPhone
  * Local storage - shows in

###

### Tags

### Recents Popover


* Document Browser API


[`UIDocumentBrowserViewController`](https://developer.apple.com/documentation/uikit/uidocumentbrowserviewcontroller)

UIDocumentPickerViewController

## Advanced

* Open-in-placed
* custom action
* opening transition

### Open-in-placed



### Custom Actions

3 diff ways.

[`UIDocumentBrowserAction`](https://developer.apple.com/documentation/uikit/uidocumentbrowseraction)


UIActivityController

### opening transition

UIDocumentBrowserTransitionController

### Demo 2

```swift
func application(_ app: UIApplication, open url: URL, options: [UIApplicationOpenURLOptionsKey : Any] = [:]) -> Bool {

    guard url.isFileURL else { return false }
    guard let dbvc = window?.rootViewController as? UIDocumentBrowserViewController else {
        return false
    }

}
```


## Thumbnail Extension

* [`QLFileThumbnailRequest`](https://developer.apple.com/documentation/quicklook/qlfilethumbnailrequest)
* [`QLThumbnailProvider`](https://developer.apple.com/documentation/quicklook/qlthumbnailprovider)
* [`QLThumbnailReply`](https://developer.apple.com/documentation/quicklook/qlthumbnailreply)


func provideThumbnail(for request: QLFileThumbnailRequest,
                    _ handler: @escaping (QLThumbnailReply?, Error?) -> Void)

## Quick-Look Preview Extension
