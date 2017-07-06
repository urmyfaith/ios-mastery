
# Role and SOP for 2-CDModel


## 1. Creating \*.xcdatamodeld file/package


## 2. Model Editing

### 2.1 creating entity

#### Entity Name

#### Class Name

`<FW>_CDModel_<EntityName>`

### 2.2 adding attributes

### 2.3 adding relationships

## 3. Creating extension for model

### readonly/derived properties

in the form of readonly properties or parameter-ful functions.

### decorating

from different source/form

if the model is multi-staged, for each named stage, there is a function for that.


## Lesson from XCL_CDModel_CLPlacemark (in XCoreLocation)

no origin (who is created it, when it is created, where is it from, why is it create) may be insufficient to represent overall use case of data.


## Attributes of CDModel roles

### Number of time to update a record .

* create-at-full, when a record is created, properties values are filled, and never updated later. Example: `Placemark_core`
* mutli-phases, there are a number of times that different properties are assigned. Noted, these are different set of properties, but each is assigned once and never update later. Example : `PlacemarkRequest`
* mutating, a certain properties' values may be updated more than once. such as `status`.

What is diff between multi-plases and mutating?
