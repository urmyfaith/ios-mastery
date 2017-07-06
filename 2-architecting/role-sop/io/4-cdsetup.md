# 4-CDSetup

One xcdatamodeld may be deployed into multiple sqlite for different dataset or different portions of entities to be used.

## Example

```swift
class FR24_CDSetup: XCL_CDSetup_base {
    override var modelName : String {
        return "" // after .xcdatamodeld
    }
    override var fileName : String {
        return "project.sqlite" //
    }
}
```
