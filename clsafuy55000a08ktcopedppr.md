---
title: "Getting Started with CSS"
seoTitle: "Getting started with css"
seoDescription: "Introduction to CSS"
datePublished: Tue Feb 06 2024 14:10:51 GMT+0000 (Coordinated Universal Time)
cuid: clsafuy55000a08ktcopedppr
slug: getting-started-with-css
tags: css3, css, getting-started-with-css

---

## Welcome to CSS

CSS is used to style the elements in a web page.

CSS is a styling language that works together with HTML to give the page its look and layout.

CSS builds on top of HTML. The **style** attribute allows you to use CSS properties to customize the visual presentation of HTML elements.

&lt;p style= "color:green"&gt; Text&lt;p&gt;

The color property is used to control the color of the text.

CSS properties control the style of HTML elements.

Examples of CSS properties are:

color

border

font-size

margin

CSS properties require values. Values are possible settings for a property.

CSS properties and values are separated by with a **colon** :

The CSS code for an HTML element must be enclosed in a single or double quotes, following the style attribute.

To apply multiple properties to an element, separate CSS properties with a **semicolon** ;

&lt;h1 style="color: yellow; background-color: blue ; text-align: center"&gt;Heading&lt;/h1&gt;

CSS stands for **CascadingStyleSheets** and is one of the 3 core web technologies.

**Cascading** refers to the set of rules that we will discuss.

## Styling Techniques

Adding CSS code to every HTML element takes time and makes your HTML structure unorganized.

When CSS is added to HTML elements, this is called inline CSS.

Inline CSS is easy to add to your code but presents some disadvantages. For example, to apply the same style to more than one html element, CSS code needs to be repeated.

An alternative styling technique is **internalCSS.**

Internal CSS is used to style the entire page.

The &lt;style&gt; container tag is added within the HTML document to group all the CSS code for the page.

&lt;head&gt;

&lt;style&gt;

p {

color: orchid;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;p&gt;Explore the city.&lt;/p&gt;

&lt;p&gt;Discover hidden gems.&lt;/p&gt;

&lt;p&gt;Take a free tour.&lt;/p&gt;

&lt;/body&gt;

The way CSS code is added depends on the styling technique you are using.

The selector in CSS code matches the HTML tags you want to target.

Selectors are used with internal CSS.

Separate multiple selectors with a comma to apply the same style to different elements. This makes your CSS code simpler.

It's best practice to include all the internal CSS code in the head of the page.

&lt;head&gt;

&lt;style&gt;

h1 {

color: orchid;

background-color: lime;

}

p{

color: orchid;

}

button {

font-size: large;

color: lightyellow;

background-color: orchid;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;h1&gt;Explore the city.&lt;/h1&gt;

&lt;p&gt;Discover hidden gems.&lt;/p&gt;

&lt;button&gt;Take a free tour&lt;/button&gt;

&lt;/body&gt;

## The Anatomy of CSS

CSS controls all the design- related aspects of your web page. This includes fonts, sizes, colors, position, spacing, layout, animations and much more.

CSS code creates **stylingrules** . The simplest styling rule consists of a selector, plus a **declaration** in **curlybraces {}.**

You can add as many declaration as you need. Each declaration should end with a semicolon;

A declaration consists of two parts: a **property** and a **value**. The property and the value inside a declaration always come in pairs.

A property: value pair in a declaration is separated with a **colon:**

Your CSS can contain as many styling rules as you need.

## Style Inheritance

When styling real pages, your CSS code can grow in length quickly.

Style inheritance enable more precise rules and write code that is simple, organized, clear and efficient.

Styling rules for parent elements will also be applied to child elements by default. This is known as **inheritance** .

Child elements inherit styles from their parents.

&lt;head&gt;

&lt;style&gt;

p{

background-color: plum;

color: darkblue;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;p&gt;Buy a ticket to &lt;b&gt;Portugal&lt;/b&gt;&lt;/p&gt;

&lt;/body&gt;

By default children inherit their parent's style. If you need a child to have a different style, you must write a separate rule for the child.

You can use a combination of selectors to make more precise rules.

The **descendant selector** target children inside a specific parent. It consists of the parent selector, followed by a space, followed by the child selector.

&lt;head&gt;

&lt;style&gt;

h1 u {

color: seagreen;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;h1&gt;Back to &lt;u&gt;school!&lt;/u&gt;&lt;/h1&gt;

&lt;p&gt;Our back to &lt;u&gt;school&lt;/u&gt; sale from July 15th.&lt;/p&gt;

&lt;/body&gt;

## ID and Class Selectors

For total control of the design of your HTML elements, you can give them IDs and classes.

IDs target specific individual element.

Classes target groups of elements.

The **id attribute** is used to give an unique identifier to a specific element in the page.

You can target specific elements using **hashtag #** followed by the ID name as a selector.

&lt;head&gt;

&lt;style&gt;

#heading {

background-color: DodgerBlue;

color: white;

text-align: center;

}

#movie {

text-align: center;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;h1 id="heading"&gt;Movie Stream&lt;/h1&gt;

&lt;h2 id="movie"&gt;Matrix&lt;/h2&gt;

&lt;p&gt;Genre: Action, Sci-fi&lt;/p&gt;

&lt;/body&gt;

Another way to identify elements is the class attribute.

Class attribute is used to apply the same style to a group of elements.

id: unique element

class: multiple elements

You can create styling rules for a group of elements in the same class (group).

Use a **dot .** followed by the class name to target all the elements in the same class.

&lt;head&gt;

&lt;style&gt;

.movie {

color: white;

background-color: navy;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;p class="movie"&gt;Avatar&lt;/p&gt;

&lt;button class="movie"&gt;Watch now&lt;/button&gt;

&lt;/body&gt;

id: #

class: .

A style rule for a class will be applied to all the elements in that class.

&lt;head&gt;

&lt;style&gt;

.intro {

color: darkblue;

font-size: 28px;

text-align: center;

}

.content {

color: seagreen;

font-size: 18px;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;h1 class="intro"&gt;Welcome to

FitLife Blog&lt;/h1&gt;

&lt;p class="content"&gt;Get inspired to lead a

healthy and active lifestyle.&lt;/p&gt;

&lt;p class="content"&gt;Explore workout routines

and nutritious recipes.&lt;/p&gt;

&lt;button class="content"&gt;Sign up&lt;/button&gt;

&lt;/body&gt;

You can also target only those elements of a specific type that have a certain class.

This CSS rule will modify only paragraphs with the **content** class.

&lt;head&gt;

&lt;style&gt;

p.content {

color: seagreen;

font-size: 18px;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;h1 class="intro"&gt;Welcome to

FitLife Blog&lt;/h1&gt;

&lt;p class="content"&gt;Get inspired to lead a

healthy and active lifestyle.&lt;/p&gt;

&lt;p class="content"&gt;Explore workout routines

and nutritious recipes.&lt;/p&gt;

&lt;button class="content"&gt;Sign up&lt;/button&gt;

&lt;/body&gt;

## Standards and Best Practices

An HTML element can be targeted for styling in different ways. For example, an element may have both a class and an ID .

&lt;p id="text1" class="info"&gt;Text&lt;/p&gt;

### Priority list

1. Inline style
    
2. IDs
    
3. Classes
    
4. Elements
    

Each type of CSS selector has its place in this priority list. When several CSS rules target the same element, the browser uses this order to determine which rule to apply.

&lt;head&gt;

&lt;style&gt;

p {

color: red;

}

#p1 {

color: blue;

}

.texts{

color: seagreen;

}

&lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;p id = "p1" class="texts"&gt;Text&lt;/p&gt;

&lt;/body&gt;

This priority order is known as **specificity**.

Specificity is the algorithm used by the browsers to determine the rule to apply to an element.

This is needed because an HTML element can be targeted in different ways.

### CSS Comments

/\*.....\*/

CSS comments need to be contained in&lt;style&gt; tags when using internal CSS.

### External CSS

An alternative to inline and internal CSS is **externalCSS**.

External CSS code is written outside the HTML document, in a separate file.

One of the advantages of external CSS is that the same CSS styles file can be used by multiple HTML documents (or web pages).

Some developers prefer external CSS because it separates structure and style into different files. This means your web page project will consist of several files with different file extensions.

External CSS is very useful for multi-page websites as you can style the entire site in one place.

You don't need &lt;style&gt; tags in an external CSS file. You can add the styling rules directly.

### Border-radius

The CSS property `border-radius: 0.3em;` is used to specify the radius of the corners of an element's border.

When you set `border-radius` to a specific value, it rounds the corners of the element's border. The value can be specified in various units, including pixels (px), ems (em), or percentages (%). In this case, `0.3em` indicates that the border radius will be 0.3 times the font size of the element.

Here's an example of how you might use `border-radius: 0.3em;` in your CSS:

```css
.element {
    border-radius: 0.3em;
}
```

In this example, any element with the class "element" will have its border corners rounded with a radius of 0.3 times the font size of the element.

You can adjust the value of `border-radius` to achieve different levels of rounding for the corners, providing various visual effects such as softer edges or circular shapes.