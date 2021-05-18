# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS


## A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5
* userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure. (Trusted domains, such as intranet sites, can store 10 times that amount. And hey, 640 KB ought to be enough for anybody.) IE does not present any form of permissions dialog, and there is no allowance for increasing the amount of storage available.

## INTRODUCING HTML5 STORAGE

* HTML5 STORAGE SUPPORT

|IE	|8.0+|
|---|--|
|**FIREFOX**|**3.5+**|
|**SAFARI**	|**4.0+**|
|**CHROME**|**4.0+**|	
|**OPERA**	|**10.5+**|
|**IPHONE**	|**2.0+**|
|**ANDROID**|**2.0+**|


## USING HTML5 STORAGE
* HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

## TRACKING CHANGES TO THE HTML5 STORAGE AREA
* The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9). Therefore, to hook the storage event, you’ll need to check which event mechanism the browser supports. (If you’ve done this before with other events, you can skip to the end of this section. Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)


**STORAGEEVENT OBJECT**

|PROPERTY|	TYPE|	DESCRIPTION|
|--|--|--|
|key	|string|	the named key that was added, removed, or modified|
|oldValue	|any|	the previous value (now overwritten), or null if a new item was added|
|newValue|	any|	the new value, or null if an item was removed|
|url*	|string	|the page which called a method that triggered this change|


## HTML5 STORAGE IN ACTION

* Let’s see HTML5 Storage in action. Recall the Halma game we constructed in the canvas chapter. There’s a small problem with the game: if you close the browser window mid-game, you’ll lose your progress. But with HTML5 Storage, we can save the progress locally, within the browser itself. Here is a live demonstration. Make a few moves, then close the browser tab, then re-open it. If your browser supports HTML5 Storage, the demonstration page should magically remember your exact position within the game, including the number of moves you’ve made, the position of each of the pieces on the board, and even whether a particular piece is selected.


**WEB SQL DATABASE SUPPORT**
|IE	|·|
|---|--|
|FIREFOX|·|	
|SAFARI	|4.0+|
|CHROME|4.0+|	
|OPERA|10.5+|
|IPHONE	|3.0+|
|ANDROID|2.0+|

## FURTHER READING

* HTML5 storage:

    * [HTML5](https://html.spec.whatwg.org/multipage/webstorage.html) Storage specification
    * [Introduction to DOM Storage](https://docs.microsoft.com/en-us/) on MSDN
    * [Web Storage: easier, more powerful client-side data storage](https://dev.opera.com/articles/web-storage/) on Opera Developer Community
    * [DOM Storage](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) on Mozilla Developer Center. (Note: most of this page is devoted to Firefox’s prototype implementation of a globalStorage object, a non-standard precursor to localStorage. Mozilla added support for the standard localStorage interface in Firefox 3.5.)
    * [Unlock local storage for mobile Web applications with HTML5](https://developer.ibm.com/technologies/web-development/) a tutorial on IBM DeveloperWorks

* Early work by Brad Neuberg et. al. (pre-HTML5):

    * [Internet Explorer Has Native Support for Persistence?!?!]() (about the userData object in IE)
    * [Dojo Storage,]() part of a larger tutorial about the (now-defunct) Dojo Offline library
    * [dojox.storage.manager API reference]()
    * [dojox.storage]() Subversion repository

* Web SQL Database:

    * [Web SQL Database]() specification
    * [Introducing Web SQL Databases]()
    * [Web Database demonstration]()
    * [persistence.js,]() an “asynchronous JavaScript ORM” built on top of Web SQL Database and Gears

* IndexedDB:

    * [Indexed Database API](https://w3c.github.io/IndexedDB/) specification
    * [Beyond HTML5: Database APIs and the Road to IndexedDB](https://hacks.mozilla.org/2010/06/beyond-html5-database-apis-and-the-road-to-indexeddb/)
    * [Firefox 4: An early walk-through of IndexedDB](https://hacks.mozilla.org/2010/06/comparing-indexeddb-and-webdatabase/)