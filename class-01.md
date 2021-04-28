

### The Structure of This Book
1- HTML
2- CSS
3- Practical

### How People Access the Web
1- Browsers
2- Web Servers
3- Screen readers
4- Devices

### How Websites Are Created
* All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more technologies into the mix.


### How the Web Works
* When you visit a website, the web server hosting that site could be anywhere in the world. In order for you to find the location of the web server, your browser will first connect to a Domain Name System (DNS) server.


### How Pages Use Structure
* The structure is very similar when a news story is viewed online (although it may also feature audio or video). This is
illustrated on the right with a copy of a newspaper alongside the corresponding article on its website.

### Structuring Word Documents
* When using a word processor to create a document, we separate out the text to give
it structure. Each topic might have a new paragraph, and each section can have a heading to describe what it covers.


### HTM L Describes the Structure of Pages

    > <html>
      <body>
      <h1>This is the Main Heading</h1>
      <p>This text might be an introduction to the rest of
      the page. And if the page is a long one it might
      be split up into several sub-headings.<p>
      <h2>This is a Sub-Heading</h2>
      <p>Many long articles have sub-headings so to help
      you follow the structure of what is being written.
      There may even be sub-sub-headings (or lower-level
      headings).</p>
      <h2>Another Sub-Heading</h2>
      <p>Here you can see another sub-heading.</p>
      </body>

![image](https://2.bp.blogspot.com/--214sLZ6XMI/WnlEESt58sI/AAAAAAAACF0/5DM2xm2ZL98kcnpC_G41lPg3ETA4ujwVgCK4BGAYYCw/s400/2.PNG)

### A Closer Look at Tags
![image](https://i.ytimg.com/vi/E53PvtDo6qE/maxresdefault.jpg)



### Attributes Tell Us More About Elements
![image](http://4.bp.blogspot.com/-p5AWmg0ysYM/VPQ5Unv5PtI/AAAAAAAAAwg/INtjtE1oAuU/s1600/4.png)



## The Evolution of HTML
* Since the web was first created, there have been several different versions of HTML.
1- HTML 4
2- XHTML 1.0
3- HTML5


#### DOCTYPEs

1. HTML5 

    > <!DOCTYPE html> 

2. HTML 4 

    >  <!DOCTYPE html PUBLIC
      "-//W3C//DTD HTML 4.01 Transitional//EN"
      "http://www.w3.org/TR/html4/loose.dtd"> 

3. Transitional XHTML 1.0

    > <!DOCTYPE html PUBLIC
      "-//W3C//DTD XHTML 1.0 Transitional//EN"
      "http://www.w3.org/TR/xhtml1/DTD/
      xhtml1-transitional.dtd">

4. Strict XHTML 1.0

    > <!DOCTYPE html PUBLIC
      "-//W3C//DTD XHTML 1.0 Strict//EN"
      "http://www.w3.org/TR/xhtml1/DTD/
      xhtml1-strict.dtd">


5. XML Declaration

    > ?xml version="1.0" ?>


#### Comme nts in HTML

     <!-- -->


#### ID Attribute
     like it  <p id="pullquote">Every time</p>


#### Class Attribute
     <p class="important">Every time</p>


#### Block Elements
      <ul>
      <li>Science: 21 Nov - 20 Feb 2010/11</li>
      <li>Architecture: 6 Mar - 15 May 2011</li>
      <li>History: 29 May - 21 Aug 2011</li>
      <li>Religion: 28 Aug - 6 Nov 2011</li>
      </ul>


#### Inline Elements

#### Grouping Text & Elements In a Block
     using it:  <div>


#### Grouping Text & Elements Inline
     using it: <span>


#### IFrames
      using it: <iframe>

#### Information About Your Pages
      using it: <meta>

***Escape characters are used to include special characters in your pages such as <, >, and ©.***


### Traditional HTML Layouts
![](http://html5doctor.com/wp-content/uploads/2009/06/html5-before1.gif)



#### Navigation
* <nav> : is used to contain the major navigational
blocks on the site such as the primary site navigation.

#### Articles
* <article> : element acts as a container for any section of a page that could stand alone and potentially be syndicated.


#### Article
* <aside> element has two purposes, depending on whether
it is inside an <article> element or not.


#### Sections
* <section> element groups related content together, and
typically each section would have its own heading.

#### Heading Groups
* <hgroup> element is to group together a set of one or more <h1> through <h6> elements so that they are treated as one single heading. 


#### Figures
* <figure> <figcaption>
* Examples of usage include:
●● Images
●● Videos
●● Graphs
●● Diagrams
●● Code samples
●● Text that supports the.


#### Sectioning El ements
* <div> element will remain an important way to group together related elements, because you should not be using
these new elements that you have just met for purposes other than those explicitly stated.


#### Linking Around Block-Level El ements
* <a> element around a block level element that contains child elements. This allows you to turn an entire block into a link.



### Who is the Site For?
* Every website should be designed for the target audience—not just for yourself or the site owner. It is therefore very important to understand who your target audience is.


### Why People Visit YOUR Website
* Now that you know who your visitors are, you need to consider why they are coming. While some people will simply chance across your website, most will visit for a specific reason.

### What Your Visitors are Trying to Achieve
*  you are looking for key tasks and motivations. This
information can help guide your site designs.

### What Information Your Visitors Need
*  you need to work out what information they need in order to achieve their goals quickly and effectively.

### How Of ten People Will Visit Your Site
* Some sites benefit from being updated more frequently than others. Some information (such as news) may be constantly changing, while other content remains relatively static.


### Site Maps
* you can start to organize the information into sections or pages.


### WireFrames
* is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require.


### Getting your message across using design
* The primary aim of any kind of visual design is to communicate. Organizing and prioritizing information on a page helps users understand its importance and what order to read it in.



# 2- JavaScript Instuctions

### 1. statement
* should end with a semicolon (;)
* each on starts on a new line 
* can be ordanized into code blocks

### 2. comments
* multi-line comment 
  * /*
  * */
* single-line comment
  * //

### 3. variable 
* var + (variable name) + (;)
* to assign them a value
  * (variable name) + (=) + (;)



## Data Type
### 1. numbers
### 2. strings
### 3. Boolean
  

>rules you must using with a variable a name:
  ```
  1.must begin with a letter, ($), (_), must not start with nummer.
  2. must not use a (-) or (.)
  3. not use keywords or reserved words 
  4. using different cases
  5. use name to describes the kind of inforimation taht thw variable stores
  6. if your variable name is made up of more than one word, use a capital letter for the first letter of every word.
  ```


## THE ABC OF PROGRAMMING:
* How do I write a script for a web page? 
 It is best to keep JavaScript code in its own JavaScript file. JavaScript files are text files (like HTML pages and CSS style sheets), but they have the .js extension.
* The HTML <script> element is used in HTML pages to tell the browser to load the JavaScript file (rather like the <link> element can be used to load a CSS file). 
* If you view the source code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.