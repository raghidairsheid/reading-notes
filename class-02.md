
# Text
* Headings and paragraphs
* Bold, italic, emphasis
* Structural and semantic markup


### Headings

![image](https://neilpatel.com/wp-content/uploads/2015/08/image354.png)

## Paragraphs
* **<p>** To create a paragraph, surround the words that make up the paragraph with an opening **<p>** tag and closing **</p>** tag.

## Bold & Italic
* **<b>** By enclosing words in the tags <b> and **</b>** we can make characters appear bold.

* **<i>** By enclosing words in the tags <i> and **</i>** we can make characters appear italic.


## Superscript & Subscript
* **<sup>** The <sup> element should be superscript such as the suffixes of dates or mathematical concepts.
![image](https://image.freepik.com/free-icon/font-style-superscript_318-48415.jpg)

* **<sub>** The <sub> element should be subscript. It is commonly used with foot notes or chemical formulas.
![image](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Format-subscript_i.svg/768px-Format-subscript_i.svg.png)

## White Space
* When the browser comes across two or more spaces next to each other, it only displays one space. Similarly if it comes across a line break, it treats that as a single space too.

## Line Breaks & Horizontal Rules
* **<br />** the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag **<br />**.

![image](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1590818624-1.jpg)

* **<hr />** To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections using the **<hr />** tag.
![image](https://www.lifewire.com/thmb/6eci9CScMDlWiITp3mEGhmrKBMw=/960x640/filters:no_upscale():max_bytes(150000):strip_icc()/hr-tag-html4-5b55ca6b46e0fb0037704508.png)


## Semantic Markup
* There are some text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages.

## Strong & Emphasis
* **<strong>** The use of the <strong> element indicates that its content has strong importance.


* **<em>** The <em> element indicates emphasis that subtly changes the meaning of a sentence.
![image](https://internetingishard.netlify.app/html-strong-emphasis-element-5b0eb2.c94cd79c.png)


## Quotations
* **<blockquote>** The <blockquote> element is used for longer quotes that take up an entire paragraph. Note how the <p> element is still used inside the <blockquote> element.

* **<q>** is used for shorter quotes that sit within a paragraph. Browsers are supposed to put quotes around the <q> element, however Internet Explorer does not — therefore many people avoid using the <q> element.

## Abb reviations & Acronyms
* **<abbr>** use an abbreviation or an acronym, then the <abbr> element can be used.

## Citations & Definitions
* **<cite>**
* **<dfn>**

## Author Details
* **<address>**

## Changes to Content
* **<ins>**
* **<del>**
*  **<s>**



# Introducing CSS
## Example Styles:
1. Boxes
2. Text
3. Specific


### Style rules with HTML elements
* selector and a declaration.


## Affect How Elements Are Displayed
* property and a value

![image](https://www.tutorialrepublic.com/lib/images/css-selector.png)

## Using External CSS
1. **<link>**
2. **href**
3. **type**
4. **rel**

## Using Internal CSS
1. **<style>**


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


## Inheritance
* If you specify the font-family or color properties on the **<body>** element, they will apply to most child elements. This is because the value of the font-family property is inherited by  hild elements.


## Why use External Style Sheets?
* When building a website there are several advantages to placing your CSS rules in a separate style sheet.