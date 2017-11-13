# b12-restapi-example.md

## Data

### Entities

Entity | Attributes / Fields | Relationships | Notes
--|--|--|--
AircraftType (Fleet?) | name, manufacture | instances
Aircraft | tailNumber | aircraftType : AircraftType
IssueType? | name
AircraftIssue
ACMSReport | | | Not standalone entity

### Views

Dashboard = caution summary + precaution summary + fleets summary (stats by fleets)

## API

Principles.

* non-standalone entity would not have api for it. such as `ACMSReport`.

individual instance can be referred with hashed value rather than sequential number, to avoid being enumerated by unwanted users.

### URL for Entities

### patterns

For entity api

* xxxs.json
* xxxs/1.json

For view api


### URL

URL | Notes
--|--
fleets.json?includes=aircraft | by default (if no includes parameter) aircrafts associated with the type is not included. , also what properties/attributes to be returned selectively.
aircrafttypes/{$hashcode}| return specific aircraft type with details.
