# Error Handling & Debugging

### JavaScript can be hard to learn and everyone makes mistakes when writing it. It will also teach you how to write scripts that deal with potential errors gracefully.

* THE CONSOLE & DEV TOOLS
* COMMON PROBLEMS
* HANDLING ERRORS


## EXECUTION CONTEXT & HOISTING
1. PREPARE
    1. The new scope is created
    2. Variables, functions, and arguments are created
    3. The value of the this keyword is determined

2. EXECUTE
    1. Now it can assign values to variables
    2. Reference functions and run their code
    3. Execute statements


## UNDERSTANDING SCOPE
* In the interpreter, each execution context has its own variables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's v a ri ables object.

## UNDERSTANDING ERRORS
* If a JavaScript statement generates an error, then it throws an exception.

## ERROR OBJECTS
* Error objects can help you find where your mistakes are and browsers have tools to help you read them.

|PROPERTY |DESCRIPTION|
|--|--|
|name |Type of execution|
|message |Description|
|fileNumber| Name of the JavaScript file|
|lineNumber| Line number of error|


---
---

|OBJECT|DESCRIPTION|
|--|--|
|Error|Generic error - the other errors are all based upon this error|
|Syntax Error|Syntax has not been followed|
|ReferenceError |Tried to reference a variable that is not declared/within scope|
|TypeError|An unexpected data type that cannot be coerced|
|URIError|encodeURI ().decodeURI(),and similar methods used incorrectly|
|EvalError|eval() function used incorrectly|


## ERROR OBJECTS CONTINUED
1. Syntax Error
2. ReferenceError
3. EvalError
4. URI Error
5. Type Error
6. RangeError
5. Error
6. NaN

## HOW TO DEAL WITH ERRORS
1. DEBUG THE SCRIPT TO FIX ERRORS
2. HANDLE ERRORS GRACEFULLY



### The JavaScript console will tell you when there is a problem with a script, where to look for the problem, and what kind of issue it seems to be.

### 1. CHROME/ OPERA

#### On a PC, press the F12 key or:

1. Go to the options menu (or three line menu icon)
2. Select **Toots** or **More tools**.
3. Select **JavaScript Console** or **Developer Tools** On a Mac press Alt + Cmd + J. Or:
4. Go to the **View** menu.
5. Select **Developer**.
6. Open the **JavaScript Console** or **Developer Tools** option and select **Console**.

### 2. INTERNET EXPLORER 
#### Press the F12 key or:
1. Go to the settings menu in the top-right.
2. Select **developer tools**.

### 3. FIREFOX
#### On a PC, press Ctrl + Shift + Kor:
1. Go to the **Firefox** menu.
2. Select **Web Developer**.
3. Open the **Web Console**.
On a Mac press Alt + Cmd + K. Or:
1. Go to the **Tools** menu.
2. Select **Web Developer**.
3. Open the **Web Console**.

### 4. SAFARI
#### Press Alt + Cmd + C or:
1. Go to the **Develop** menu.
2. Select **Show Error Console**.
If the **Develop** menu is not shown:
1. Go to the **Safari** menu.
2. Select **Preferences**.
3. Select **Advanced**.
4. Check the box that says **"Show Develop menu in menu bar."**

### LOGGING DATA TO THE CONSOLE

        console.log ()

1. The first line is used to indicate the script is running.
2. Next an event handler waits for the user leaving a text input, and logs the va lue that they entered into that form field.
3. That the user clicked submit
4. The value in the width input
5. The value in the height input
6. The value of the area variable

### MORE CONSOLE METHODS
1. `conso1e.info()` can be used for general information
2. `console.warn()` can be used for warnings
3. `console.error()` can be used to hold errors


### WRITING ON A CONDITION
1. Below, when users leave an input, the code checks to see if they entered a value that is 10 or higher. If not, it will write a message to the screen.

2. The second check looks to see if the calculated area is a numeric value. If not, then the user must have entered a value that was not a number.


### BREAKPOINTS

### 1. `CHROME`
1. Select the Sources option.
2. Select the script you are working with from the left-hand pane. The code will appear to the right.
3. Find the line number you want to stop on and click on it.
4. When you run the script, it will stop on this line. You can now hover over any variable to see its value at that time in the script's execution.
### 2. `FIREFOX`
1. Select the Debugger option.
2. Select the script you are working with from the left-hand pane. The code will appear to the right.
3. Find the line number you want to stop on and click on it.
4. When you run the script, it will stop on this line. You can now hover over any variable to see its value at that time in the script's execution.

### HANDLING EXCEPTIONS

            try {
                // Try to execute this code
            } catch (exception) {
                // If there is an exception, run this code
            } finally {
                // This always gets executed
            }


### THROWING ERRORS
* To create your own error, you use the following line:

            throw new Error( "message") ;

### DEBUGGING TIPS
1. another browser.
2. add numbers
3. strip it back
4. explaining the code
5. search
6. code playgrounds
7. validation tools
8. JavaScript
9. json
10. jQuery


### COMMON ERRORS
1. GO BACK TO BASICS
2. MISSED/ EXTRA CHARACTERS
3. DATA TYPE ISSUES