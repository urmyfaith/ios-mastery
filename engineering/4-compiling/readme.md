

## http://news.realm.io/news/swift-at-scale

They have a problem to Swift migrate a big codebase, with tons of errors needing to be solved before being compiled again.

I have some thoughts on the problems that they were facing.

For Swift migration, with a lot of errors and warnings, we can,

* create smaller projects that use part of the code base. migrate smaller projects one by one,
