# 6-MKMapViewAgent

An agent is a *subcontractor* to `MKMapViewManager`. As a subcontractor, it shares a part of `MKMapViewManager`'s duties, namely:


* setupMapView, to hook gesture recognizers if applicable
* viewForAnnotation, for certain types of annotation
* rendererForOverlay, for certain types of overlays
* transform business objects into `MKAnnotation` and `MKOverlay`, and add/or remove them into/from mapView.
  * managing the mapping between business object/model and view model objects.

## Can-do and execute

An agent is designed to target specific business objects, so that it cannot handle others. The way to express its ability, is to return a tuple with first element Bool to tell whether it can handle the case, and the second element as result itself. As shown below:

```swift

func viewForAnnotation(_ annotation : MKAnnotation) -> (Bool, MKAnnotationView?)


func rendererForOverlay(_ overlay : MKOverlay) -> (Bool, MKOverlayRenderer?)

```
