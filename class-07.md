
# What's a Table?
* A table represents information in a grid format.

![](https://th.bing.com/th/id/OIP.8wqylrd1maM47zzp9nl9KwAAAA?w=144&h=186&c=7&o=5&pid=1.7)

* Basic Table Structure

        <table>
        <tr>
        <td>

* Table Headings

        <th>

* Long Tables

        <thead>
        <tbody>
        <tfoot>


---

# The Document Object Model (or DOM) 
* is the document object. 
* It represents the web page loaded into the current browser window or tab. 




| `PROPERTY`|`DESCRIPTION`|
|--|--|
|document.title|Title of current document|
|document. l astModified|Date on which document was last modified|
|document .URL|Returns string containing URL of current document|
|document.domain|Returns domain of current document|

---
---
---


|`METHOD`| `DESCRIPTION`|
|--|--|
|document.write()| Writes text to document|
|document.getElementByld()|Returns element, if there is an element with the value of the id attribute that matches |
|document.querySe1ectorA11() |Returns list of elements that match a CSS selector, which is specified as
a parameter |
|document.createElement() |Creates new element|
|document.createTextNode() |Creates new text node |


## Global object: String object

| `PROPERTY`| `DESCRIPTION`|
|--|---|
|length |Returns number of characters in the string in most cases|

---
---
---

|`METHOD` |`DESCRIPTION`|
|--|--|
|toUpperCase() |Changes string to uppercase characters|
|tolowerCase() |Changes string to lowercase characters|
|charAt()|Takes an index number as a parameter, and returns the character found at that position.|
|indexOf()|Returns index number of the first time a character or set of characters is found within the string.|
|lastlndexOf()|Returns index number of the last time a character or set of characters is found within the string.|
|substring()|Returns characters found between two index numbers where the character for the first index number is included and the character for the last index number is not included|
|split()|When a character is specified, it splits the string each time it is found, then stores each individual part in an array|
|trim()|Removes whitespace from start and end of string|
|replace()|Like find and replace, it takes one value that should be found, and another to replace it (by default, it only replaces the first match it finds)|



## Data types **revisited** 
* simple (or primitive) data types:
    1. String
    2. Number
    3. Boolean
    4. Undefined
    5. Null

* complex data type:

    6. 0bject

## Global object: Number object


|`METHOD`|`DESCRIPTION`|
|--|--|
|isNaN()|Checks if the value is not a number|
|toFixed()|Rounds to specified number of decimal places (returns a string)|
|toPrecision()|Rounds to total number of places (returns a st ring)|
|toExponentia1()|Returns a string representing the number in exponential notation|


## Global object: Math object

|`PROPERTY`|`DESCRIPTION`|
|--|--|
|Math.PI |Returns pi (approximately 3.14159265359)|
---
---
--

|`METHOD` |`DESCRIPTION`|
|--|--|
|Math.round()| Rounds number to the nearest integer|
|Math.sqrt(n) |Returns square root of positive number, e.g.: Math.sqrt(9) returns 3|
|Math.ceil()| Rounds number up to the nearest integer|
|Math.floor()|Rounds number down to the nearest integer|
|Math.random()|Generates a random number between0 (inclusive) and 1(not inclusive)|

 

## Global object: Data object(and Time)



|`METHOD` |`DESCRIPTION`|
|--|--|
|getDate()   ,   setDate() |Returns / sets the day of the month (1-31)|
|getDay() |Returns the day of the week (0-6)|
|getFullYear()   ,   setFullYear() |Returns / sets the year (4 digits)|
|getHours() , setHours()|Returns / sets the hour (0-23)|
|getMilliseconds() , setMilliseconds() |Returns / sets the milliseconds (0-999)|
|getMinutes() , setMinutes()| Returns / sets the minutes (0-59)|
|getMonth() , setMonth()|Returns/ sets the month (0-11)|
|getSeconds() , setSeconds() |Returns / sets the seconds (0-59)|
|getTime() , setTime()|Number of milliseconds since January 1, 1970,00:00:00 UTC (Coordinated Universal Time) and a negative number for any time before|
|getTimezoneOffset()| Returns time zone offset in mins for locale|
|toDateString() |Returns "date" as a human-readable string|
|toTimeString() |Returns "time" as a human-readable string| 
|toString()|Returns a string representing the specified date|


 


 ---
 ---



### Creating an object: Constructor Notation


### Updating an object

### Creating many object: Constructor Notation


# Stroing Data:
1. variables
2. arrays



* individual object
* multiple object

## THREE GROUPS OF BUILT-IN OBJECTS:
1. USING BUILT-IN OBJECTS:
- The three built-in each offer a different range of tools that help you write scripts
2. BROWSER OBJECT MODEL: 
- The Brueser Object Medel creates a medel of the brewser tab or window.



             WINDOW
                DOCUMENT
                HISTORY
                LOCATION
                NAVIGATOR
                SCREEN
    

## The Browser Object Model :The window object

|`PROPERTY`|`DESCRIPTION`|
|--|--|
|window.innerHeight|Height of window (excluding browser chrome/user interface) (in pixels)|
|window.innerWidth|Width of window (excluding browser chrome/user interface) (in pixels)|
|window.pageXOffset|Distance document has been scrolled horizontally (in pixels)|
|window. pageYOffset|Distance document has been scrolled vertica lly (in pixels)|
|window.screenX|X-coordinate of pointer, relative to top left corner of screen (in pixels)|
|window.screenY|Y-coordinate of pointer, relative to top left corner of screen (in pixels)|
|window.location|Current URL of window object (or local file path)|
|window.document|Reference to document object, which is used to represent the current page contained in window|
|window.history|Reference to history object for browser window or tab, which contains details|
|window.history.length|Number of items in hi story object for browser window or tab|
|window.screen|Reference to screen object|
|window.screen.width|Accesses screen object and finds value of its width property (in pixels)|
|window.screen.height|Accesses screen object and finds value of its height property (in pixels)|

---
---
---

|`METHOD`|`DESCRIPTION`|
|--|--|
|window.alert()|Creates dialog box with message (user must click OK button to close it)|
|window.open()|Opens new browser window with URL specified as parameter (if browser has pop-up blocking software installed, this method may not work).|
|window.print()|Tells browser that user wants to print contents of current page (acts like user has clicked a print option in the browser's user interface)|






 