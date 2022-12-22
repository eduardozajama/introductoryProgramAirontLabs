# 14. Flexbox and Grid

## One vs. Two Dimensions
The most important thing to know is that flexbox is one-dimensional, while CSS Grid is two-dimensional. Flexbox lays out items along either the horizontal or the vertical axis, so you have to decide whether you want a row-based or a column-based layout.
![](/studyMaterial/14-flexboxAndGrid/twodimensions.png)

A flex layout can also wrap in multiple rows or columns and flexbox treats each row or column as a separate entity, based on its content and the available space.

On the other hand, CSS Grid lets you work along two axes: horizontally and vertically. Grid allows you to create two-dimensional layouts where you can precisely place grid items into cells defined by rows and columns.

This is how W3C wants us to use flexbox and Grid, however practice frequently overrides theory and not everyone is fan of the one-dimensional vs. two-dimensional narrative.
>[More About Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

>[A great tool to practice](https://flexboxfroggy.com/)

# Basic concepts of grid layout
CSS Grid Layout introduces a two-dimensional grid system to CSS. Grids can be used to lay out major page areas or small user interface elements. This article introduces the CSS Grid Layout and the new terminology that is part of the CSS Grid Layout Level 1 specification. The features shown in this overview will then be explained in greater detail in the rest of this guide.

## What is a grid?
A grid is a set of intersecting horizontal and vertical lines defining columns and rows. Elements can be placed onto the grid within these column and row lines. CSS grid layout has the following features:

### Fixed and flexible track sizes
You can create a grid with fixed track sizes – using pixels for example. This sets the grid to the specified pixel which fits to the layout you desire. You can also create a grid using flexible sizes with percentages or with the fr unit designed for this purpose.

### Item placement
You can place items into a precise location on the grid using line numbers, names or by targeting an area of the grid. Grid also contains an algorithm to control the placement of items not given an explicit position on the grid.

### Creation of additional tracks to hold content
You can define an explicit grid with grid layout. The Grid Layout specification is flexible enough to add additional rows and columns when needed. Features such as adding "as many columns that will fit into a container" are included.

 ### Alignment control
Grid contains alignment features so we can control how the items align once placed into a grid area, and how the entire grid is aligned.

### Control of overlapping content
More than one item can be placed into a grid cell or area and they can partially overlap each other. This layering may then be controlled with the z-index property.

### Grid is a powerful specification that, when combined with other parts of CSS such as flexbox, can help you create layouts that were previously impossible to build in CSS. It all starts by creating a grid in your grid container.

### Grid container
We create a grid container by declaring display: grid or display: inline-grid on an element. As soon as we do this, all direct children of that element become grid items.

## Resources
>[Mozilla dev](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)

>[Design Blog](https://webdesign.tutsplus.com/articles/flexbox-vs-css-grid-which-should-you-use--cms-30184)

>[Hubspot blog](https://blog.hubspot.com/website/css-grid-vs-flexbox)

