API Plan
========

The root of the application will revolve around an API. This API will 
be built on a RESTful PHP MVC framework. Data will be encapsulated in 
valid JSON for transport. Authentication will mimic oAuth 1.0A for 
launch, and later will be converted to a meed full oAuth 2.0 spec.

> TableTalk: Your Social Dining Experience

API Methods
===========

**Authentication**
* __userLogin__(username, password, timestamp)
* __userLogout__(username, oAuthIdent, timestamp)
* __createHash__(username, password, timestamp)
* __sessionHeartbeat__(username, oAuthIdent)

**User Accounts**
* __userCreate__(username, password, timestamp, ...)
* __userDelete__(username, password, timestamp, ...)
* __userUpdate__(username, oAuthIdent, timestamp, ...)
* __userAccount__(username, oAuthIdent, ...)

**User Social Actions**
* __addToFavorites__(username, oAuthIdent, addRemove, ...)
* __delFromFavorites__(username, oAuthIdent, addRemove, ...)
* __shareThis__(username, oAuthIdent, ...)
* __postReview__(username, oAuthIdent, ...)

**User In-Restaurant Actions**
* __fetchRestaurantPreferences__(...)
* __checkIn__(username, oAuthIdent, restaurant, ...)
* __checkOut__(username, oAuthIdent, restaurant, ...)
* __tagWaiter__(username, oAuthIdent, waiter, ...)
* __msgWaiter__(username, oAuthIdent, waiter, ...)
* __fetchMenu__(username, oAuthIdent, restaurant, ...)
* __fetchMyOrder__(username, oAuthIdent, restaurant, ...)
* __addToOrder__(username, oAuthIdent, restaurant, ...)
* __viewBill__(username, oAuthIdent, restaurant, ...)
* __getBill__(username, oAuthIdent, waiter, ...)
* __payBill__(username, oAuthIdent, restaurant, ...)
* __pushSuggestionToOtherPatrons__(username, oAuthIdent, ...)
* __pushChatMessageToOtherPatrons__(username, oAuthIdent, ...)

------------------------

**Restaurant Accounts**
* __viewAccount__(username, oAuthIdent, ...)
* __delAccount__(username, password, ...)
* __viewReviews__(username, oAuthIdent, ...)
* __pushSpecialOffer__(username, oAuthIdent, ...)
* __pushSuggestion__(username, oAuthIdent, ...)
