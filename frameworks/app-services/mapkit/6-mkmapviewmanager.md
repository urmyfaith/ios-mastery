

# 6-MKMapViewManager

A Manager is a *contractor* for UIVC or alike. It manages, but not owns, a [`MKMapView`](https://developer.apple.com/documentation/mapkit/mkmapview) objects for its full features. It implements [`MKMapViewDelegate`](https://developer.apple.com/documentation/mapkit/mkmapviewdelegate)


```swift


```


## Base classes


* NSObject
  * XMK_MKMapViewManager_base : MKMapViewDelegate
    * XMK_MKMapViewManager_agents_base

### XMK_MKMapViewManager_base

weak var mapView : MKMapView?

func setupMapView(_ mv : MKMapView)

func teardownMapView()

### XMK_MKMapViewManager_agents_base

var agent_ = [XMK_MKMapViewAgent]()

override func setupMapView(_ mv: MKMapView)

func mapView(_ mapView: MKMapView, viewFor annotation: MKAnnotation) -> MKAnnotationView?

func mapView(_ mapView: MKMapView, rendererFor overlay: MKOverlay) -> MKOverlayRenderer

## Example/Subclass

search `_MKMapViewManager_`
