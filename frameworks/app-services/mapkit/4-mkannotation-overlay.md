

## Custom Overlay

Naive case: If your map need polyline to represent a single path, you can create MKPolyline and add it to map.

Real cases: However, there are times more than one path need to be represented; also wall or boundary of objects need to be represented as polyline too. By then you cannot use built-in MKPolyline alone. Here are few options of solutions.

* use one of concrete classes as [`MKOverlay`](https://developer.apple.com/documentation/mapkit/mkoverlay)
