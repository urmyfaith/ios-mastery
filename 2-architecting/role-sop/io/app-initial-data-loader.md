
# App initial data loader

* created and used in AppDelegate (or should it be singleton?)
* detecting first launch after app installation and upgrade. Acts only needed.
* creating the local folders and files (including sqlite/CoreData files) for app to use.
* data source can be (1) in bundle, (2) from server/iCloud, or (3) randomly created.
* supports pruning/reset.


## Plus

* for each launch, or long time background, update data content periodically with server.
