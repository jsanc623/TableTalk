API Plan
========

The root of the application will revolve around an API. This API will 
be built on a RESTful PHP MVC framework. Data will be encapsulated in 
valid JSON for transport. Authentication will mimic oAuth 1.0A for 
launch, and later will be converted to a meed full oAuth 2.0 spec.

API Methods
===========

array array_fill ( int $start_index , int $num , mixed $value )

> **Authentication**
>> userLogin (username, password, timestamp)
* userLogout(username, oAuthIdent, timestamp)

> **User Accounts**
* userCreate(username, password, timestamp, ...)
* userDelete(username, password, timestamp, ...)
* userUpdate(username, oAuthIdent, timestamp, ...)
* fetchData (username, oAuthIdent, ...)

> **User Actions**
* modifyFavorites(username, oAuthIdent, timestamp, (bool)addRemove, ...)


> **Restaurant Accounts**
* 
