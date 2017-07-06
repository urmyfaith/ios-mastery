# SOP-3-CDStore

## 0. Naming and file location


`<FW>_CDStore_<EntityName>`

## 1. import

```swift
import CoreData
import CoreLocation
```

## 2. superclass and setup

* NSObject
  * XCL_CDStore_base
    * XCL_CDStore_entityClass_base<EntityClass> : XCL_CDStore_base where EntityClass : NSManagedObject

```swift


```

## 3. customization

### 3.1 init

```swift
override init() {
    super.init()
    entityName = "" // as entity name
    attr_primary_sort = "" // 'An instance of NSFetchedResultsController requires a fetch request with sort descriptors'
}
```

### 3.2 create and decorate

### 3.3 list

#### semantic predicate/count/list

some set of records have named meaning. An eum can be defined for them.

```swift
enum Situation {
    case all
    case waiting
    case done
    case error
}
```

And the NSPredicate for each case can be defined centrally.

```swift
func predicate(situation s: Situation) -> NSPredicate? {

    switch s {
    case .all: return nil
    case .waiting : return NSPredicate(format: "mark == nil")
    case .done : return NSPredicate(format: "mark == %@", "done")
    case .error : return NSPredicate(format: "mark == %@", "error")
    }
}
```

Followed by count and list

```swift
func list(situation s : Situation) -> [XCL_CDModel_CLPlacemark] {

    guard let ctx = cdContext else { fatalError() }
    let fr : NSFetchRequest<XCL_CDModel_CLPlacemark> = XCL_CDModel_CLPlacemark.fetchRequest()
    fr.predicate = self.predicate(situation: s)
    let result_ = try! ctx.fetch(fr)
    return result_
}

func count(situation s : Situation) -> Int {
    let p = predicate(situation: s)
    return super.count(predicate: p)
}

```
