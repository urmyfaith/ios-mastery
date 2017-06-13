


## Making properties KVO

### for all properties to be kvo'ed, mark them as dynamic


```swift

dynamic var error : Error?

```


### struct

CANNOT  make property type as optional of struct type, that is, you must make type as struct (such as Int) and give it a default value.

### enum

'@objc' enum must declare an integer raw type

### @obj class - not effective.
