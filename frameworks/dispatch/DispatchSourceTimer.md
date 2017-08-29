

# [`DispatchSourceTimer`](https://developer.apple.com/documentation/dispatch/dispatchsourcetimer)


```swift


timer = DispatchSource.makeTimerSource()
timer?.scheduleOneshot(deadline: DispatchTime.now() + 1)
        timer?.setEventHandler(handler: {

            if let r = self.store.getNextUnprocessed() {
                self.processSingle(r)
            }

        })
        timer?.resume()

```

## Refs


https://www.cocoawithlove.com/blog/2016/07/30/timer-problems.html
