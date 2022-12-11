# 9.CSS
## What is CSS?
Cascading Style Sheets, fondly referred to as CSS, is a simple design language intended to simplify the process of making web pages presentable.

CSS handles the look and feel part of a web page. Using CSS, you can control the color of the text, the style of fonts, the spacing between paragraphs, how columns are sized and laid out, what background images or colors are used, layout designs,variations in display for different devices and screen sizes as well as a variety of other effects.

CSS is easy to learn and understand but it provides powerful control over the presentation of an HTML document. Most commonly, CSS is combined with the markup languages HTML or XHTML.

## Advantages of CSS
CSS saves time − You can write CSS once and then reuse same sheet in multiple HTML pages. You can define a style for each HTML element and apply it to as many Web pages as you want.

Pages load faster − If you are using CSS, you do not need to write HTML tag attributes every time. Just write one CSS rule of a tag and apply it to all the occurrences of that tag. So less code means faster download times.

Easy maintenance − To make a global change, simply change the style, and all elements in all the web pages will be updated automatically.

Superior styles to HTML − CSS has a much wider array of attributes than HTML, so you can give a far better look to your HTML page in comparison to HTML attributes.

Multiple Device Compatibility − Style sheets allow content to be optimized for more than one type of device. By using the same HTML document, different versions of a website can be presented for handheld devices such as PDAs and cell phones or for printing.

Global web standards − Now HTML attributes are being deprecated and it is being recommended to use CSS. So its a good idea to start using CSS in all the HTML pages to make them compatible to future browsers.


CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.
``` CSS
p { font-family: Arial;}
```

CSS declarations sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.

``` CSS
h1, h2, h3 { font-family: Arial; color: yellow;}
```
## How to use CSS
There are three ways you can use to implement CSS into your HTML: internal, external, and inline styles. Let’s break them down.

## Internal CSS
Internal or embedded CSS requires you to add 
```<style>```  tag in the ```<head>``` section of your HTML document.

This CSS style is an effective method of styling a single page. However, using this style for multiple pages is time-consuming as you need to put CSS rules on every page of your website.

Here’s how you can use internal CSS:

1. Open your HTML page and locate <head> opening tag.
2. Put the following code right after the <head> tag

```CSS
<style type="text/css">
```
3. Add CSS rules on a new line. Here’s an example:
```CSS
body {
    background-color: blue;
}
h1 {
    color: red;
    padding: 60px;
}
```
4. Type the closing tag:
```CSS
</style>
```
Your HTML file will look like this:
```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
    background-color: blue;
}
h1 {
    color: red;
    padding: 60px;
} 
</style>
</head>
<body>

<h1>Airont Labs Bootcamp</h1>
<p>This is our paragraph.</p>

</body>
</html>
```
### Advantages of Internal CSS:

You can use class and ID selectors in this style sheet. Here’s an example:
```CSS
.class {
    property1 : value1; 
    property2 : value2; 
    property3 : value3; 
}

#id {
    property1 : value1; 
    property2 : value2; 
    property3 : value3; 
}

```
Since you’ll only add the code within the same HTML file, you don’t need to upload multiple files.

### Disadvantages of Internal CSS:

Adding the code to the HTML document can increase the page’s size and loading time.

## External CSS
With external CSS, you’ll link your web pages to an external .css file, which can be created by any text editor in your device (e.g., Notepad++).

This CSS type is a more efficient method, especially for styling a large website. By editing one .css file, you can change your entire site at once.

Follow these steps to use external CSS:
1. Create a new .css file with the text editor, and add the style rules. For example:
```CSS
.xleftcol {
   float: left;
   width: 33%;
   background:#809900;
}
.xmiddlecol {
   float: left;
   width: 34%;
   background:#eff2df;
}


```
In the ```<head>``` section of your HTML sheet, add a reference to your external .css file right after ```<title>``` tag:

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```
Don’t forget to change style.css with the name of your .css file.

### Advantages of External CSS:
Since the CSS code is in a separate document, your HTML files will have a cleaner structure and are smaller in size.
You can use the same .css file for multiple pages.
### Disadvantages of External CSS:
Your pages may not be rendered correctly until the external CSS is loaded.
Uploading or linking to multiple CSS files can increase your site’s download time.

## Inline CSS
Inline CSS is used to style a specific HTML element. For this CSS style, you’ll only need to add the style attribute to each HTML tag, without using selectors.

This CSS type is not really recommended, as each HTML tag needs to be styled individually. Managing your website may become too hard if you only use inline CSS.

However, inline CSS in HTML can be useful in some situations. For example, in cases where you don’t have access to CSS files or need to apply styles for a single element only.

Let’s take a look at an example. Here, we add an inline CSS to the ```<p> ```and ```<h1>``` tag:
```html
<!DOCTYPE html>
<html>
<body style="background-color:black;">

<h1 style="color:white;padding:30px;">Airont Labs Bootcamp</h1>
<p style="color:white;">Something useful here.</p>

</body>
</html>

```
### Advantages of Inline CSS:
You can easily and quickly insert CSS rules to an HTML page. That’s why this method is useful for testing or previewing the changes, and performing quick-fixes to your website.
You don’t need to create and upload a separate document as in the external style.
### Disadvantages of Inline CSS:
Adding CSS rules to every HTML element is time-consuming and makes your HTML structure messy.
Styling multiple elements can affect your page’s size and download time.

## CSS Selectors
There are many different typesof CSS selector that allo w you to target rules to specific elements in an HTML document.
CSS selectors are case sensitive, so they must match element names and attribute values
exactly.
There are some more advanced selectors which allow you to select elements based on attributes and their values.

>[Cheatsheet](https://www3.cs.stonybrook.edu/~pramod.ganapathi/doc/CSE102/CSE102-CheatSheetCSSLong.pdf)

At some point, you will be working on a project and you will find that the CSS you thought should be applied to an element is not working. Often, the problem is that you create two rules that apply different values of the same property to the same element. Cascade and the closely-related concept of specificity are mechanisms that control which rule applies when there is such a conflict. The rule that's styling your element may not be the one you expect, so you need to understand how these mechanisms work.

Also significant here is the concept of inheritance, which means that some CSS properties by default inherit values set on the current element's parent element and some don't. This can also cause some behavior that you might not expect.
## Cascade
Stylesheets cascade — at a very simple level, this means that the origin, the cascade layer, and the order of CSS rules matter. When two rules from the same cascade layer apply and both have equal specificity, the one that is defined last in the stylesheet is the one that will be used.

> [More about Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)

## Specificity
Specificity is the algorithm used by browsers to determine the CSS declaration that is the most relevant to an element, which in turn, determines the property value to apply to the element. The specificity algorithm calculates the weight of a CSS selector to determine which rule from competing CSS declarations gets applied to an element.

### How is specificity calculated?
Specificity is an algorithm that calculates the weight that is applied to a given CSS declaration. The weight is determined by the number of selectors of each weight category in the selector matching the element (or pseudo-element). If there are two or more declarations providing different property values for the same element, the declaration value in the style block having the matching selector with the greatest algorithmic weight gets applied.

The specificity algorithm is basically a three-column value of three categories or weights - ID, CLASS, and TYPE - corresponding to the three types of selectors. The value represents the count of selector components in each weight category and is written as ID - CLASS - TYPE. The three columns are created by counting the number of selector components for each selector weight category in the selectors that match the element.

#### Selector weight categories
The selector weight categories are listed here in the order of decreasing specificity:

#### ID column
Includes only ID selectors, such as #example. For each ID in a matching selector, add 1-0-0 to the weight value.

#### CLASS column
Includes class selectors, such as .myClass, attribute selectors like ``` [type="radio"]``` and ```[lang|="fr"]``` , and pseudo-classes, such as ```:hover```, ```:nth-of-type(3n)```, and ```:required```. For each class, attribute selector, or pseudo-class in a matching selector, add 0-1-0 to the weight value.

#### TYPE column
Includes type selectors, such as p, h1, and td, and pseudo-elements like ``` ::before```, ```::placeholder```, and all other selectors with double-colon notation. For each type or pseudo-element in a matching selector, add 0-0-1 to the weight value.

#### No value
The universal selector (*) and the pseudo-class ```:where()``` and its parameters aren't counted when calculating the weight so their value is 0-0-0, but they do match elements. These selectors do not impact the specificity weight value.

Combinators, such as +, >, ~, " ", and ||, may make a selector more specific in what is selected but they don't add any value to the specificity weight.

The negation pseudo-class, ```:not()```, itself has no weight. Neither do the ```:is()``` or the ```:has()``` pseudo-classes. The parameters in these selectors, however, do. The values of both come from the parameter in the list of parameters that has the highest specificity. The :not(), :is() and :has() exceptions are discussed below.

>[More about Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

## Box model
When laying out a document, the browser's rendering engine represents each element as a rectangular box according to the standard CSS basic box model. CSS determines the size, position, and properties (color, background, border size, etc.) of these boxes.

Every box is composed of four parts (or areas), defined by their respective edges: the content edge, padding edge, border edge, and margin edge.
 ![Box Model](/studyMaterial/9-css/boxmodel.png)

### Content area
The content area, bounded by the content edge, contains the "real" content of the element, such as text, an image, or a video player. Its dimensions are the content width (or content-box width) and the content height (or content-box height). It often has a background color or background image.

If the box-sizing property is set to content-box (default) and if the element is a block element, the content area's size can be explicitly defined with the width, min-width, max-width, height, min-height, and max-height properties.
### Padding area
The padding area, bounded by the padding edge, extends the content area to include the element's padding. Its dimensions are the padding-box width and the padding-box height.

The thickness of the padding is determined by the padding-top, padding-right, padding-bottom, padding-left, and shorthand padding properties.

### Border area
The border area, bounded by the border edge, extends the padding area to include the element's borders. Its dimensions are the border-box width and the border-box height.

The thickness of the borders are determined by the border-width and shorthand border properties. If the box-sizing property is set to border-box, the border area's size can be explicitly defined with the width, min-width, max-width, height, min-height, and max-height properties. When there is a background (background-color or background-image) set on a box, it extends to the outer edge of the border (i.e. extends underneath the border in z-ordering). This default behavior can be altered with the background-clip CSS property.
### Margin area
The margin area, bounded by the margin edge, extends the border area to include an empty area used to separate the element from its neighbors. Its dimensions are the margin-box width and the margin-box height.

The size of the margin area is determined by the margin-top, margin-right, margin-bottom, margin-left, and shorthand margin properties. When margin collapsing occurs, the margin area is not clearly defined since margins are shared between boxes.

Finally, note that for non-replaced inline elements, the amount of space taken up (the contribution to the height of the line) is determined by the line-height property, even though the borders and padding are still displayed around the content.
## Resources

>[Developer Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

>[Tutorialspoint](https://www.tutorialspoint.com/css/what_is_css.htm)

>[Hostinger](https://www.hostinger.com/tutorials/difference-between-inline-external-and-internal-css#)

>[Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)















