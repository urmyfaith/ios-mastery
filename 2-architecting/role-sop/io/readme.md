
# Whole picture of CoreData related roles

## 2-CDModel

## 3-CDStore

## 4-CDSetup



## CDModel vs CDStore


property| CDModel | CDStore
--|--|--
calling cdContext save() | No | Yes
mutation method name | decorate | update
scope | a single object itself |  entity-wide , many objects
knowing entity name| No | Yes, in init()
values | defines values, such as CLError.Code | not care 
