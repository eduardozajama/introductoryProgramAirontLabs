# 12. Media Queries
CSS Media queries are a way to target browser by certain characteristics, features, and user preferences, then apply styles or run other code based on those things. Perhaps the most common media queries in the world are those that target particular viewport ranges and apply custom styles, which birthed the whole idea of responsive design.
```javascript

/* When the browser is at least 600px and above */
@media screen and (min-width: 600px) {
  .element {
    /* Apply some styles */
  }
}
```

There are lots of other things we can target beside viewport width. That might be screen resolution, device orientation, operating system preference, or even more among a whole bevy of things we can query and use to style content.

## Using media queries
Media queries are commonly associated with CSS, but they can be used in HTML and JavaScript as well.
## Anatomy of a Media Query
Now that we’ve seen several examples of where media queries can be used, let’s pick them apart and see what they’re actually doing.
![MediaQuery](/studyMaterial/12-mediaqueries/media-query-anatomy.webp)


# CSS Units
Whenever you build a website on any website builder you may see that some elements offer size choices, such as PX, EM, REM, percent, VW, or VH while margin or padding any content.
The most important aspect to learn about the different units is that some units, such as PX are absolute units, and some are relative units.

## Absolute Units
PX:  Pixels (px) are considered absolute units, although they are relative to the DPI and resolution of the viewing device. But on the device itself, the PX unit is fixed and does not change based on any other element. Using PX can be problematic for responsive sites, but they are useful for maintaining consistent sizing for some elements. If you have elements that should not be resized, then using PX is a good choice.

## Relative Units
EM: Relative to the parent element

REM: Relative to the root element (HTML tag)

%: Relative to the parent element

VW: Relative to the viewport’s width

VH: Relative to the viewport’s height

Unlike PX, relative units like %, EM, and REM are better suited to responsive design and also help meet accessibility standards. Relative units scale better on different devices because they can scale up and down according to another element’s size.

## When Should You Use One Unit Over Another?
Ultimately, there isn’t a perfect answer for this question. In general, it is often best to choose one of the relative units over PX so that your web page has the best chance of rendering a beautifully responsive design. Choose PX however, if you need to ensure that an element never resizes at any breakpoint and remains the same regardless of whether a user has chosen a different default size. PX units ensure consistent results even if that’s not ideal.

EM is relative to the parent element’s font size, so if you wish to scale the element’s size based on its parent’s size, use EM.

REM is relative to the root (HTML) font size, so if you wish to scale the element’s size based on the root size, no matter what the parent size is, use REM. If you’ve used EM and are finding sizing issues due to lots of nested elements, REM will probably be the better choice.

VW is useful for creating full width elements (100%) that fill up the entire viewport’s width. Of course, you can use any percentage of the viewport’s width to achieve other goals, such as 50% for half the width, etc.

VH is useful for creating full height elements (100%) that fill up the entire viewport’s height. Of course, you can use any percentage of the viewport’s height to achieve other goals, such as 50% for half the height, etc.

% is similar to VW and VH but it is not a length that is relative to viewport’s width or height. Instead, it is a percentage of the parent element’s width or height. Percentage units are often useful to set the width of margins, as an example.

## Resources
>[css guide ](https://essential-addons.com/elementor/css-design-guide-difference/)

>[frecodecamp](https://www.freecodecamp.org/news/learn-css-units-em-rem-vh-vw-with-code-examples/)

>[Media Queries guide](https://css-tricks.com/a-complete-guide-to-css-media-queries/#aa-display-quality)

>[w3schools](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
