# What is HTML

HTML is an acronym which stands for Hyper Text Markup Language which is used for creating web pages and web applications.

## HTML Elements
An HTML file is made of elements. These elements are responsible for creating web pages and define content in that webpage. An element in HTML usually consist of a start tag ``` <tag name>,``` close tag ``` </tag name> ``` and content inserted between them. Technically, an element is a collection of start tag, attributes, end tag, content between them.

```html
<!DOCTYPE html>  
<html>  
<head>  
    <title>WebPage</title>  
</head>  
<body>  
   <h1>This is my first web page</h1>  
    <h2> How it looks?</h2>  
     <p>It looks Nice!!!!!</p>  
</body>  
</html> 

```
```<!DOCTYPE>``` : It defines the document type or it instruct the browser about the version of HTML.

```<html >``` :This tag informs the browser that it is an HTML document. Text between html tag describes the web document. It is a container for all other elements of HTML except <!DOCTYPE>

```<head>```: It should be the first element inside the ```<html> ```element, which contains the metadata(information about the document). It must be closed before the body tag opens.

```<title>```: As its name suggested, it is used to add title of that HTML page which appears at the top of the browser window. It must be placed inside the head tag and should close immediately. (Optional)

```<body> ```: Text between body tag describes the body content of the page that is visible to the end user. This tag contains the main content of the HTML document.

```<h1> ```: Text between ``` <h1> ```tag describes the first level heading of the webpage.

```<h2>``` : Text between ```<h2>``` tag describes the second level heading of the webpage.

```<p> ```: Text between ```<p>``` tag describes the paragraph of the webpage.

## Meta tag


The ```<meta>``` tag defines metadata about an HTML document. Metadata is data (information) about data.
```html
<head lang="en">
  <meta http-equiv="content-language" content="en">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="keywords" content="website, blog, foo, bar">
  <meta name="author" content="John Doe">
  <meta name="publisher" content="John Doe">
  <meta name="copyright" content="John Doe">
  <meta name="description" content="This short description describes my website.">
   <meta name="page-topic" content="Media">
  <meta name="page-type" content="Blogging">
  <meta name="audience" content="Everyone">
  <meta name="robots" content="index, follow">
  
  <title>My website title</title>
</head>

```

## What is the HTML input element?

The <input> element is most commonly used for collecting and retrieving user data from a web form.

It's where users enter their data.

```html
<input type="value"> <!-- the value of the type attribute determines the style of input field -->
```

## Input types
|type=" "   |Description
|-------|-------
|text |Defines a one-line text input field
|password|Defines a one-line password input field
|submit |Defines a submit button to submit the form to server
|reset |Defines a reset button to reset all values in the form.
|radio |Defines a radio button which allows select one option.
|checkbox |Defines checkboxes which allow select multiple options form.
|button |Defines a simple push button, which can be programmed to perform a task on an event.
|file |Defines to select the file from device storage.
|image |Defines a graphical submit button.


HTML5 added new types on ```<input>``` element. Following is the list of types of elements of HTML5


|type=" " |Description
|------|----
|color |Defines an input field with a specific color.
|date |Defines an input field for selection of date.
|datetime-local |Defines an input field for entering a date without time zone.
|email |Defines an input field for entering an email address.
|month |Defines a control with month and year, without time zone.
|number |Defines an input field to enter a number.
|url |Defines a field for entering URL
|week |Defines a field to enter the date with week-year, without time zone.
|search |Defines a single line text field for entering a search string.
|tel |Defines an input field for entering the telephone number.

## What is the Diffreence Between XHTML and HTML5?
XHTML is a combination of HTML and XML, while HTML5 is a version of HTML. XHTML has its own parsing requirements, while HTML does not have any specific requirements and uses its own. Know more about what is the difference between XHTML and HTML5 from the table below.

|XHTML |HTML5
|---|---
|Extensible HyperText Markup Language|Later version of HyperText Markup Language
|More extensive doc |Much simple than XHTML
|Every element should have the corresponding ending tag|Closing tag can be omitted if required
|No tags are used for header, footer, section, article, nav, and divs with classes; instead, ids have to be used|Tags are used for header, footer, section, article, and ​nav, thus making it easier to write and read code
|Is case-sensitive|Not case-sensitive
|Does not support any Geo-Location API|Includes an API that enable the users to share their location
|Internet Explorer 8 Browser does not support this|Is compatible with all browsers
|Better suited for desktop computers|More compatible with mobile devices — smartphones and tablets







