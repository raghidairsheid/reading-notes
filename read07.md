




# CSS
- allows to create rules that specify how the content of an element should appear.



### thinking inside the box:
* imagine that there is an invisible box around every HTML element.

  * you can create rules that control the way that each individual box (and the contents of that box) is presented.



  > example styles

### block and inline elements

|Block elements|Inline elements |
|--- |---| 
|look like they start on a new line. | flow within the text and do not start on a new |
|<h1> ,<h6> , <p> , <div> | <b>, <i>, <img>, <em> ,<span>|


## CSS associates Style rules with HTML elements:
* CSS rule contains two parts: a **selector** and a **declaration**.
  *example:*    

    > p {font-family: Arial;}
    > **p**: is the selector
    > **{font-family: Arial;}** : is the declaration


## CSS Properties affect how Elements are displayed:
* declarations sit inside curly brackets and each is made up of two parts: a **property** and a **value**, separated by a colon.
  *example:*

    > h1, h2, h3 {font-family: Arial; color: yellow;}
    > **font-family:** $ **color:** is the property
    > **Arial;** $ **yellow;** is the value

## Using External CSS
1- **<link>**

  - can be used in an HTML document to tell the browser where to find the CSS file used to style the page
- href

  - specifies the path
- type

  - specifies the type of document being linked to, The value should be text/css.
- rel

  - specifies the relationship between the HTML page and the file it is linked to, the value should be stylesheet.

  *example:*

     > <link href="css/styles.css" type="text/css" rel="stylesheet" />


2-  **<**  **Style**  **>** 

- should use the type attribute to indicate
that the styles are specified in CSS. The value should be text/css.
  *example:*

     > *<* *style type="text/css"* *>*


## CSS Selectors:

|Selectors | Example |
|---|---|
|Universal Selector |  * {} |
| Type Selector | h1, h2, h3 {}  |
| Class Selector | .note {} |
| ID Selector | #introduction {} |
| Child Selector | li>a {} |
|Descendant Selector | p a {} |
|Adjacent Sibling Selector | p a {} |
|General Sibling Selector | h1~p {} |


### Why use External Style Sheets?

1. All of your web pages can share the same style sheet.
2. This means that the same code does not need to be repeated in every page (which results in less code and smaller HTML pages).
3. once the user has downloaded the CSS stylesheet, the rest of the site will load faster.
4. considered good practice to have the content of the site separated from the rules that determine how it appears.


## **Sometimes you might consider placing CSS rules in the same page as your HTML code.**

#Color
#### Color can really bring your pages to life.


## Foreground Color
* specify the color of text inside an element:
  * rgb values :

  >rgb(100,100,90)

  * hex codes
  > #ee3e80
  
  * color names
  > DarkCyan

## Background Color
  * like it: background-color


## Opacity color
* opacity, rgba

## HSL Colors
* hue
* saturation
* ligh tness

## HSL & HSLA
* like it: hsl(0,0%,78%);