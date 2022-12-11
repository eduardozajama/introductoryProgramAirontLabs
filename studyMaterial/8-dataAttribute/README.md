# 8. Data- attributes
## Definition and Usage
The data-* attribute is used to store custom data private to the page or application.

The data-* attribute gives us the ability to embed custom data attributes on all HTML elements.

The stored (custom) data can then be used in the page's JavaScript to create a more engaging user experience (without any Ajax calls or server-side database queries).

The data-* attribute consist of two parts:

The attribute name should not contain any uppercase letters, and must be at least one character long after the prefix "data-"
The attribute value can be any string

Note: Custom attributes prefixed with "data-" will be completely ignored by the user agent.

The data-* attribute is a Global Attribute, and can be used on any HTML element.

## Creating an HTML Data Attribute
Adding a data attribute is easy. Any HTML element can have any number of data attributes added to its opening tag. We simply type data- followed by the name of our attribute into the element's opening tag alongside any other attributes we're already using.

For example, let's create a data attribute called "badges" and use it to attach a number to a p element.

``` html 
<p data-badges="3">This is a paragraph element.</p>

```

### Resources

>[w3schools](https://www.w3schools.com/tags/att_data-.asp)

>[dev.to](https://dev.to/sprite421/how-to-use-html-data-attributes-adc)

