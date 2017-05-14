

## For Framework developer

If your framework is using other concurrency (own or recursive calling a dispatch queue) framework, or owning its own dispatch queue, then you need to do following.

* privatizing your own queue for internal use only.
* ask for this framework's user to provide his queue, let's call it client queue, so that in callbacks will be run on client queue. Make it optional as property, not check it strictly later.
* for any asynchronous operations ,
  * when it starts, check the presence of client queue, if not there, treat it as an programming error to throw.
  * at results time, then calling client's callback in client queue.  


This design is to ensure the developer would not make the common mistakes of forgetting async back to his own queue in framework's callbacks.


## For Application developer (Framework users)

If the framework you are using follow the rules above, then let the framework object know your current queue as client queue.

Otherwise, you need to remember to async back to your own queue when framework's callbacks are invoked.


## WWDC

* [2016 720]
* [2015 718]
