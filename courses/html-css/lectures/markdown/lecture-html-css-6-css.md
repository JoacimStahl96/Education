### 6.HTML & CSS
#### Cascading Style Sheets


---

#### HTML, CSS and JavaScript
* HTML is used to create the basic structure and content of a webpage (the skeleton).
* **CSS is used for the design of a webpage – where everything is placed and how it looks (body).**
* JavaScript is used to define the interactive elements of a webpage making it dynamic (muscles).


---

#### What is CSS?
* CSS stands for Cascading Style Sheets.
* A Style Sheet is a collection of style rules.
* CSS describes how HTML elements are to be displayed on screen, paper, or in other media.
* CSS associates style rules with HTML elements.
* CSS rules can be applied on just one or multiple HTML elements.


---

#### Examples of different styles
* Color
* Background color
* Size
* Font
* Border


---

####  CSS example




---

#### CSS Example
<img src="/media/html-css-images/html-css-5/box.png" alt="div with styles">


---

#### Web page with CSS
<img src="/media/html-css-images/html-css-5/withCSS.png" alt="web page with css">


---

#### Web page without CSS
<img src="/media/html-css-images/html-css-5/withoutCSS.png" alt="web page without css">


---

####  Selectors and Declarations

* The selector indicates which element the CSS rule applies to.
* The declaration indicates how the element should be styled.



---

####  CSS can be added to HTML elements in 3 ways

* Inline - by using the style attribute in HTML elements.
* Internal - by using a ```<style>``` element in the ```<head>``` section.
* External - by using an external CSS file.



---

####  Inline CSS
* Inline CSS applies a unique style to a single HTML element.
* Inline CSS uses the style attribute.



---

####  Internal Style sheet
* Internal style sheets may be used if one single page has a unique style.



---

####  External Stylesheet
* External style sheets are used to define the style for one or many HTML pages.
* This means that external style sheets can change the look of an entire web site, by changing one file!
* To use an external style sheet, add a link to it in the ```<head>``` section of the HTML page.
```
<body>
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>
```



---

####  External Stylesheet

```CSS
/* styles.css */
body {
  background-color: powderblue;
}

h1 {
  color: blue;
}

p {
  color: red;
}
```



---

#### Invisible box around every element
* Every element has an invisible box around them.
<img src="/media/html-css-images/html-css-5/invisBox.png" alt="invisible element boxes">


---

#### Block and Inline elements
* Block-level elements always starts on a new line and takes up the full width available.
* Inline elements does not start on a new line and only takes up as much width as necessary.
* Elements are one of the options by default but the style can be overwritten.


---

#### Block and Inline elements
<img src="/media/html-css-images/html-css-5/inline.png" alt="inline & block elements">


---

####  HTML - id attribute
* An id is an unique identifier for an HTML element (within the same HTML document).
* This id can be used by CSS and JavaScript to perform certain tasks for that element.
* In CSS, the (#) character, followed by the id is used to select that element.

```HTML
<style>
  #identified {
    background-color: skyblue;
  }
</style>

<div id="identified">This div has a special ID on it!</div>
<div>This is just a regular div.</div>
```
[Test on w3schools](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_id_css)



---

####  HTML - class attribute
* The class attribute is used to define equal styles for elements with the same class name.
* Meaning that all HTML elements with the same class can have the same format and style.



---
```HTML
<head>
  <style>
    .myClass {
      background-color: black;
      color: white;
    }
  </style>
</head>
<body>
  <div class="myClass">
    <h2>Header 1</h2>
  </div>

  <div class="myClass">
    <h2>Header 2</h2>
  </div>

  <div class="myClass">
    <h2>Header 3</h2>
  </div>
</body>
```



---

####  Different Selectors
```CSS
h2 { /* Selector */
  color: #ff00ff;
}
```



---

#### ## Universal selector

```CSS
/* Targets all elements on page. */
* {
  color: #ff00ff;
}
```
#### ## Type selector

```CSS
/* Targets all h1 elements on page. */
h1 {
  color: #ff00ff;
}
```



---

#### ## Class Selector

```CSS
/* Targets all elements with a matching class. */
.myClass {
  color: #ff00ff;
}
```
#### ## Id selector
```CSS
/* Targets THE element with a specific id. */
#myId {
  color: #ff00ff;
}
```



---

#### ## Child Selector

```CSS
/* Targets an element that is a direct child. */
.myClass>a {
  color: #ff00ff;
}
```
#### ## Decendant selector
```CSS
/* Targets any matching element that is a decendent of another. */
.myClass a {
  color: #ff00ff;
}
```



---

#### Default styles
* Browsers are setting default styles to elements.
* These are not the same in different browsers.
* <a href="http://hg.mozilla.org/mozilla-central/file/tip/layout/style/res/html.css" target="_blank">Firefox default HTML stylesheet</a>
* <a href="http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css" target="_blank">WebKit default HTML stylesheet</a>


---

#### CSS in devtools
* In all browsers you can in see and change the styling of a website in devtools.
* Let's try it!


---

#### CUT!


---

####  Inheritence
* Styling can be inherited from parents of child elements.

```HTML
<!-- The color of the paragraph will be red, since it inherits the color from the parent div-->
<div>
  <p>Hello World!</p>
</div>
```

```CSS
/* styles.css */
div {
  color: red;
}
```

---

####  Comments in CSS
In CSS we use /* to open and */ to close a comment

```CSS
/* This is a comment */
body {
  background-color: powderblue;
}

/*
multi
lint
comment
*/
```



---

#### CSS Versions
* CSS1 (1996)
* CSS2 (1998)
* CSS3 <a href="https://caniuse.com/#search=css3" target="_blank">Browser support</a>
* CSS4


---

#### Validating CSS code
  * To make sure that your CSS code is valid and correct you can validate your code using different software.
  * <a href="https://jigsaw.w3.org/css-validator/#validate_by_uri">Link to online CSS validator</a>