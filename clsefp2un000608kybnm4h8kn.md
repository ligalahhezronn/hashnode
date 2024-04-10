---
title: "CSS Page Design and Layout"
seoTitle: "CSS Page Design and Layout"
seoDescription: "CSS Page Design and Layout"
datePublished: Fri Feb 09 2024 09:17:22 GMT+0000 (Coordinated Universal Time)
cuid: clsefp2un000608kybnm4h8kn
slug: css-page-design-and-layout
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1707470185186/71cfdf3d-a775-41a0-aef8-bb28dd1b4960.png
tags: css

---

## The Box Model

The **Box Model** is a way of thinking about how HTML elements are displayed on a web page.

The Box Model treats each HTML element as a rectangular box with 4 layers.

The **content box** is the innermost layer where content like text and images appears.

&lt;p&gt; Discounts &lt;/p&gt;

The content of the HTML element above is **Discounts**.

The **width** and **height** properties set the size of the content box for an element.

An HTML element can be classified into **inline** and **block**\-**elements**.

By default, when width and height have not been set, block-level elements take up the full width available.

The full width available for a block-level element is given by it's parent.

By default, inline elements such as images and links, have a content layer that takes up as much width as necessary to display the content. They don't make use of all the available space given by the parent.

The text-align property aligns text within the content box of an element.

By default, the border will be applied on the edges of the box content, unless padding has been added. The padding layer is wrapped around the content box to create an extra space within the element and push the border outward.

.padded-box {

border: 2px solid #FFA310;

padding: 20px;

color: #FFFFFF;

}

.default-box {

border: 2px solid #FFA310;

color: #FFFFFF;

}

**Border** is the 3rd layer. It surrounds the padding.

By default, the padding value for most HTML elements is 0.

You can have different padding values to each of the 4 sides. Add 4 values separated by the spaces in the order: **top**, **right**, **bottom**, **left**.

Use padding-top, padding-right, padding-bottom, padding-left to target specific sides.

To calculate the total box dimensions, you need to add the dimensions of the three layers: content, padding and border.

**Margin** is the outermost layer in the box model. It wraps around the border layer and is transparent.

Use the margin property to create an extra space outside elements, between the border and other elements,and prevent overlap.

## Flexbox Layout

Modern websites are designed to look great on any device, regardless of screen dimensions.

The **display** property can override the default behavior of inline and block elements.

a {

display: block;

border: #4478B1 solid;

text-decoration: none;

}

The flex layout makes it easy to build and design responsive pages. It creates a row or a column layout.

Flexbox is used to arrange items inside a container automatically. To create a flex (flexible) container, set the display property to flex.

div {

border: 1px solid rgb(189, 185, 185);

box-shadow: 0 2px 4px #000000;

display: flex

;

}

By default, child items inside a flex parent container are arranged automatically in one row, trying to make the best use of the available space.

By default, child items in a flex container are arranged in a row (horizontally). Set the **flex**\-**direction** sub-property to **column** to arrange the items vertically inside a flex container.

.container-row {

display: flex;

flex-direction: row;

border: 1px solid red;

margin-bottom: 25px;

}

.container-column {

display: flex;

flex-direction: column;

border: 1px solid blue;

}

By default, child items in a flex container will all try to fit into one line. You can change that and allow the items to wrap as needed in the **flex**\-**wrap** sub-property. Again, items will be arranged automatically and the number of lines will depend on the size of the screen.

#wrap {

padding: 20px;

margin-bottom: 10px;

border: 1px solid rgb(189, 185, 185);

display: flex;

flex-wrap: wrap;

}

#nowrap {

padding: 20px;

border: 1px solid rgb(189, 185, 185);

display: flex;

flex-wrap: nowrap;

}

By default, child items inside a flex container will be arranged automatically. The space each item takes up will depend on it's content. So it's possible that some items are displayed bigger than others if they have more content.

To have more control over the space items take inside a flex container, you can set the **flex**\-**grow** sub-property.

The flex-grow sub-property gives an item the ability to grow to take up more space when this space is available in the container (bigger screen). It accepts a unit less value as a proportion.

#container {

border: 1px solid #818181;

box-shadow: 2px 2px #474747;

display: flex;

}

#item1 {

flex-grow: 1;

border: 1px solid #868686;

box-shadow: 2px 2px black;

margin-right: 10px;

margin-left: 5px;

}

#item2 {

flex-grow: 2;

border: 1px solid #868686;

box-shadow: 2px 2px black;

margin-right: 10px;

}

#item3 {

flex-grow: 3;

border: 1px solid #868686;

box-shadow: 2px 2px black;

margin-right: 5px;

}

The flex-grow sub-property allows items in a flex container to take up more space in bigger screens.

The possible values for flex-grow are whole non-negative numbers. These are unitless values that serve as proportions for the dimensions of the items.

By default, items inside a flex container have a flex-grow value of 0. This means that when there is a bigger space (like in a bigger screen) they won't always grow.

**flex**\-**shrink** does the opposite of flex-grow. It is used to adopt your design to smaller screens.

The value determines how much a flex item will shrink relative to the rest of the items when there isn't enough space in the flex container.

A higher value means the item will shrink more.

The default value for flex-shrink is 1.

## Positioning

By default, all elements are positioned **static.**

This means they are not positioned in any specific way, and the browser will display them one after the another in the order they appear in the HTML code.

You can give elements an exact position (in to the top-left corner of the page) using pixels as **coordinates**.

The x (or horizontal) axis goes from left to right. The y (or vertical) axis goes from top to bottom.

The **position** property gives you more control to place HTML elements in your designs.

You can give elements an exact position on the page using **absolute** positioning.

Then you can add the horizontal and vertical coordinates as pixels, using **left** and **top**.

#item1 {

position:absolute;

left: 10px;

top: 20px;

}

Positioning an HTML element means positioning one of it's corners.

Applying **property**: **absolute**; to an element takes the element out of it's static flow (element order).

In the example below, the second element is absolutely positioned, this means it's no longer the second item in the flow.

/\* Default static position \*/

#item1 {

background-color: #0000FF;

height: 100px;

width: 300px;

}

/\* Absolute positioning \*/

#item2 {

position: absolute;

left: 50px;

top: 40px;

background-color: #FF0000;

height: 100px;

width: 300px;

}

An element with **position**: **fixed**; always stays in the same place even if the page is scrolled.

Use relative position to reposition an element without taking it out of the static flow (the default element order). Relative positioned items take the static position as a reference. So the top-left corner of the static position becomes the new reference.

.special {

background-color: #FFD700;

position: relative;

/\*shift from left;\*/

left:20px;

}

To precisely position child element in relation to the parent, set the parent to **position**: **relative**; This makes the left corner of the parent box the new reference point.

#parent {

border:solid;

width: 150px;

height: 80px;

left: 40px;

top: 60px;

position: relative;

}

#child {

position:absolute;

top: 10px;

left: 20px

}

If none of the ancestors have their position set to relative, then the reference point for posting is the body (parent of all elements).

In addition to top and left, you can use bottom and right to control the position of the elements.

### justify-content

The CSS property `justify-content: space-between;` is used within a flex container to distribute its flex items evenly along the main axis, with the first item aligned to one edge of the container and the last item aligned to the opposite edge.

When you set `justify-content` to `space-between`, it adds equal spacing between the flex items, effectively pushing them as far apart from each other as possible while still keeping the first and last items flush against the edges of the container.

Here's an example of how you might use `justify-content: space-between;` in your CSS:

```css
.container {
    display: flex;
    justify-content: space-between;
}
```

In this example, any element with the class "container" becomes a flex container, and its child elements will be distributed along the main axis with equal space between them. The first item will be flush against the start edge of the container, and the last item will be flush against the end edge.

This property is commonly used for creating layouts where you want to maximize space between flex items, such as navigation menus or grid-like structures.

## Backgrounds

Backgrounds can make a dramatic impact on a website's overall look and feel.

Th CSS property that sets the color of the background for an element is **background**\-**color**.

You can add an image as the background for an element!

body {

background-image: url('https://blob.learn.com/courses/coffee.jpeg');

}

The &lt;div&gt; will help you apply backgrounds to groups of elements or different sections of your page.

If the image is smaller than the space you want to fill with it, the image will be repeated (or tiled) by default to cover all the painting area.

You can set the **background**\-**repeat** to **no**\-**repeat**, this way the image will only appear once ( in the top-left corner) and the box painting area won't necessarily be fully covered.

Use the repeat-x or repeat-y to control the tiling direction.

.box1 {

background-image: url('https://blob.learn.com/courses/logo1.png');

background-repeat: repeat-x;

height: 150px;

width: 150px;

border: 1px solid;

margin-bottom: 10px;

}

.box2 {

background-image: url('https://blob.learn.com/courses/logo1.png');

background-repeat: repeat-y;

height: 150px;

width: 150px;

border: 1px solid;

}

The background-position property can take pixels, percentages, and words like top, left, right, bottom, center.

#box1 {

background-image: url('https://learnassets.azureedge.net/sl-logo.png');

background-repeat: no-repeat;

background-position: bottom center;

height:150px;

padding: 10px;

margin-bottom: 15px;

border: 1px solid black;

}

#box2 {

background-image: url('https://learnassets.azureedge.net/sl-logo.png');

background-repeat: no-repeat;

background-position: top right;

height:150px;

padding: 10px;

border: 1px solid black;

}

The **background**\-**size** property controls the dimensions of the background image. The first value represents the width, and the second value represents the height.

The background-size property has two other possible values to control how the image fits inside the box. Neither of them alters the aspect ratio.

**contain** scales the image to ensure that the entire image is shown as big as possible. This can result in tiling or empty space.

**cover** scales the image to completely cover all the painting area. Potentially showing only part of the image if proportions differ.