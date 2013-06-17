API Plan
========

The root of the application will revolve around an API. This API will 
be built on a RESTful PHP MVC framework. Data will be encapsulated in 
valid JSON for transport. Authentication will mimic oAuth 1.0A for 
launch, and later will be converted to a meed full oAuth 2.0 spec.

TableTalk > Social Dining Experience
------------------------------------

API Methods
===========

**Authentication**
* userLogin (username, password, timestamp)
* userLogout(username, oAuthIdent, timestamp)
* createHash(username, password, timestamp)
* sessionHeartbeat(username, oAuthIdent)

**User Accounts**
* userCreate(username, password, timestamp, ...)
* userDelete(username, password, timestamp, ...)
* userUpdate(username, oAuthIdent, timestamp, ...)
* userAccount(username, oAuthIdent, ...)

**User Social Actions**
* addToFavorites(username, oAuthIdent, addRemove, ...)
* delFromFavorites(username, oAuthIdent, addRemove, ...)
* shareThis(username, oAuthIdent, ...)
* postReview(username, oAuthIdent, ...)

**User In-Restaurant Actions**
* fetchRestaurantPreferences(...)
* checkIn(username, oAuthIdent, restaurant, ...)
* checkOut(username, oAuthIdent, restaurant, ...)
* tagWaiter(username, oAuthIdent, waiter, ...)
* msgWaiter(username, oAuthIdent, waiter, ...)
* fetchMenu(username, oAuthIdent, restaurant, ...)
* fetchMyOrder(username, oAuthIdent, restaurant, ...)
* addToOrder(username, oAuthIdent, restaurant, ...)
* viewBill(username, oAuthIdent, restaurant, ...)
* getBill(username, oAuthIdent, waiter, ...)
* payBill(username, oAuthIdent, restaurant, ...)
* pushSuggestionToOtherPatrons(...)
* pushNotification(...)
* pushUpdate(...)

------------------------

**Restaurant Accounts**
* viewAccount(username, oAuthIdent, ...)
* delAccount(username, password, ...)
* viewReviews(username, oAuthIdent, ...)
* pushSpecialOffer(username, oAuthIdent, ...)
* pushSuggestion(username, oAuthIdent, ...)
