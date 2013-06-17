API Plan
========

The root of the application will revolve around an API. This API will 
be built on a RESTful PHP MVC framework. Data will be encapsulated in 
valid JSON for transport. Authentication will mimic oAuth 1.0A for 
launch, and later will be converted to a meed full oAuth 2.0 spec.

API Methods
===========

[code]
> **Authentication**
* userLogin (username, password,   timestamp)
* userLogout(username, oAuthIdent, timestamp)

> **User Accounts**
* userCreate(username, password,   timestamp, ...)
* userDelete(username, password,   timestamp, ...)
* userUpdate(username, oAuthIdent, timestamp, ...)
* fetchData (username, oAuthIdent, ...)

> **User Actions**
* userAddToFavorites(username, oAuthIdent, timestamp, restaurantData, otherData...)
* userRemoveFromFavorites(username, oAuthIdent, timestamp, restaurantData, otherData...)


> **Restaurant Accounts**
* 
[/code]
