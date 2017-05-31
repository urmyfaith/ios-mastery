

# Codegen for Entity

Options

* Manual/None
* Class Definition
* Category/Extension


## Category/Extension

Developer should write the class definition, which could be as simple as below.

```swift
import CoreData
class XCL_CDModel_CMAltitudeData: NSManagedObject {

}

```

Xcode generates code like below

```swift
// XCL_CDModel_CMAltitudeData+CoreDataProperties.swift

extension XCL_CDModel_CMAltitudeData {

    @nonobjc public class func fetchRequest() -> NSFetchRequest<XCL_CDModel_CMAltitudeData> {
        return NSFetchRequest<XCL_CDModel_CMAltitudeData>(entityName: "CMAltitudeData")
    }

    @NSManaged public var pressure: NSNumber?
    @NSManaged public var relativeAltitude: NSNumber?
    @NSManaged public var timestamp: NSDate?

}
```
