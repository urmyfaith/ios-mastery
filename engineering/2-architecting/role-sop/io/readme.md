# Roles for IO 

Following concerns are covered in IO part.

- (Data) Format, for file storage and network transmission.
- Data Generator (rule-based and randon/noise) (Non-media data)
- Data Emitter (from sensors)


Families By Persistence Media and Technology

- FS 
- URL
- CD


## Format 

Format for storage. Loosely speaking, there are at least 2 purposes for string/text. One is to interact with user to read and input/select. The other is for formatting the data structure or model, to be saved in file or transmitted via network. 


## Kinds of persistence media 

- Local
  - File
  - CoreData
- Remote
  - HTTP/URL
  - iCloud or CloudKit
  - TCP/IP


## 3-DataGenerator 

## 3-Emitter (from Sensors)

## FS (File System) family 

## CD (CoreData) family


Tier|[FS (File System)](fs)|[URL](url)|[CD (CoreData)](cd)|Sensing
---|---|---|---|---
2|Format|URLRequestFactory|CDModel<br/>CDModelDict
3|Addressor, FSLoader|URLCommand, URLErrorHandler|CDStore<br/>CDImporter<br/>CDExporter|Emitter
4||URLDirector
