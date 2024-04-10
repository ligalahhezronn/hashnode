---
title: "Html5"
seoTitle: "html 5, html"
seoDescription: "HTML 5"
datePublished: Mon Feb 05 2024 04:45:55 GMT+0000 (Coordinated Universal Time)
cuid: cls8g8lax000a0ajs15pphpho
slug: html5
tags: html, html5

---

When writing html5 documents, one of the first new features that you'll notice is the doc type declaration:

&lt;!DOCTYPE HTML&gt;

The character encoding (charset) declaration is also simplified:

&lt;meta charset="UTF-8"&gt;

### New elements in html5

article aside audio canvas details datalist embed footer header nav output progress section video and even more!

The default character encoding in html5 is UTF-8

## New in html5

The web forms 2.0 specification allows for creation of more powerful forms and more compelling user experiences.

Date pickers, color pickers, and numeric stepper controls have been added.

Input field types now include emails, search and URL.

PUT and DELETE from methods are now supported.

### Integrated API (Application Programming Interfaces)

Drag and drop

Audio and video

Offline web applications

History

Local storage

Geolocation

Web messaging

## Content models

In html, elements typically belonged in either the block level or inline content model.

Html5 introduces seven main content models.

Metadata

Embedded

Interactive

Heading

Phasing

Flow

Sectioning

Html5 content models are designed to make the markup structure more meaningful for both the browser and the web designer.

### Metadata

Content that sets up the presentation or behavior of the rest of the content.

These elements are found in the head of the document.

&lt;base&gt;, &lt;link&gt;, &lt;meta&gt;, &lt;noscript&gt;, &lt;script&gt;, &lt;title&gt;, &lt;style&gt;

### Embedded

Content that imports other resources into the document.

&lt;svg&gt;, &lt;iframe&gt;, &lt;math&gt;&lt;audio&gt;, &lt;video&gt;, &lt;object&gt;, &lt;canvas&gt;, &lt;img&gt;

### Interactive

Content specifically intended for user interaction.

&lt;a&gt;, &lt;audio&gt;, &lt;video&gt;, &lt;button&gt;, &lt;details&gt;, &lt;embed&gt;, &lt;iframe&gt;, &lt;img&gt;, &lt;input&gt;, &lt;label&gt;, &lt;object&gt;, &lt;select&gt;,&lt;textarea&gt;

### Heading

Defines a section header.

&lt;h1&gt;, &lt;h2&gt;, &lt;h3&gt;, &lt;h4&gt;, &lt;h5&gt;&lt;h6&gt;, &lt;hgroup&gt;

### Phasing

This model has a number of inline level elements in common with html4.

&lt;img&gt;, &lt;span&gt;, &lt;strong&gt;, &lt;label&gt;, &lt;br /&gt;, &lt;small&gt;, &lt;sub&gt; and more.

The same element can belong to more than one content model.

### Flow content

Contains the majority of HTML5 elements that would be included in the normal flow of the document.

### Sectioning content

Define the scope of headings, content, navigation and footers.

&lt;article&gt;, &lt;aside&gt;, &lt;nav&gt;, &lt;section&gt;

The various content models overlap in certain areas depending on how they are being used.

## HTML5 Page Structure

You may not need some elements depending on your page structure

&lt;header&gt; - contains the brandings like logo.

&lt;nav&gt; - contains navigational section of the site.

&lt;article&gt; - web page main content.

&lt;section&gt; - divide section of main content.

&lt;aside&gt; - contains extra information and related content or link.

&lt;footer&gt; - information about copyright, privacy policy, terms of use, etc.

### Header, nav and footer

In html4, we would define a header like this

&lt;div I'd="header"&gt;

In html5 a simple header tag is used instead.

The &lt;header&gt; element is appropriate for use inside the body tag.

The header is completely different from the head tag.

Footer

The footer element is also widely used.

Generally, we refer to a section located at the very bottom of a web page as the footer.

&lt;footer&gt;...&lt;/footer&gt;

The following information is usually provided between these tags:

* Contact information
    
* Privacy policy
    
* Social media icons
    
* Terms of service
    
* Copyright information
    
* Sitemap and related documents
    

Nav

&lt;nav&gt;

This tag represent a section of a page that links to other pages or to certain sections within the page. This would be a section with navigation links.

Not all of the links in a document should be inside the nav element. The nav element is intended only for major blocks of navigation links. Typically, the &lt;footer&gt; element often has a list of links that doesn't have to be in a &lt;nav&gt; element.

### Article, section and aside

&lt;article&gt;

Article is a self-contained, independent piece of content that can be used and distributed separately from the rest of the page or site. This could be a forum post, a magazine or a newspaper article, a blog entry, a comment, an interactive widget or gadget, or any other independent piece of content.

The &lt;article&gt; element replaces the &lt;div&gt; element that was widely used in html4, a long with an id or class.

&lt;article&gt;

&lt;h1&gt;The article title&lt;/h1&gt;

&lt;p&gt;Contents of the article element &lt;/p&gt;

&lt;/article&gt;

When an article element is nested, the inner element inner element represents an article related to the outer element. For example blog post comments can be &lt;article&gt; elements nested in the &lt;article&gt; representing the blog post.

Section

&lt;section&gt; is a logical container of the web page or article.

Sections can be used to divide up content within an article.

For example, a homepage could have a section for introducing the company, another for news items, and still another for contact information.

Each &lt;section&gt; should be identified typically by including a heading (h1-h6 element) as a child of the section element.

&lt;article&gt;

&lt;h1&gt;Welcome&lt;/h1&gt;

&lt;section&gt;

&lt;h1&gt;Heading&lt;/h1&gt;

&lt;p&gt;content or image&lt;/p&gt;

&lt;/section&gt;

&lt;/article&gt;

It makes sense to separately syndicate the content of a section element, use an article element instead.

Aside

&lt;aside&gt;

Is secondary or tangential content which would be considered separate from but indirectly related to the main content. This type of content is often represented in sidebars.

When an &lt;aside&gt; tag is used within an&lt;article&gt; tag, the content of &lt;aside&gt; should be specifically related to that article.

&lt;article&gt;

&lt;h1&gt; Gifts for everyone&lt;/h1&gt;

&lt;p&gt;This website will be the best place for choosing gifts&lt;/p&gt;

&lt;aside&gt;

&lt;p&gt;Gifts will be delivered to you within 24 hours&lt;/p&gt;

&lt;/aside&gt;

&lt;/article&gt;

When an &lt;aside&gt; tag is used outside an &lt;article&gt; tag, it's content should be related to the surrounding content.

## The audio element

Before html5, there was no standard for playing audio files on a web page. The html5 &lt;audio&gt; element specifies a standard for embedding audio in a web page.

There are two different ways to specifies the audio source file's URL. The first uses the source attribute:

&lt;audio src="http://www.learn.com/uploads/audio.mp3" controls&gt;

Audio element not supported by your browser

&lt;/audio&gt;

The second way uses the &lt;source&gt; element inside the &lt;audio&gt; element:

&lt;audio controls&gt;

&lt;source src="http://www.learn.com/uploads/audio.mp3" type="audio/mpeg"&gt;

&lt;source src="http://www.learn.com/uploads/audio.ogg" type="audio/ogg"&gt;

&lt;/audio&gt;

Multiple&lt;source&gt; elements can be linked to different audio files. The browser will use the first recognized format.

The &lt;audio&gt; element creates an audio player inside the browser.

The text between the &lt;audio&gt; and &lt;/audio&gt; tags will be displayed in browsers that do not support the &lt;audio&gt; element.

### Attributes of audio

controls

Specifies that audio controls should be displayed.

autoplay

Audio starts playing as soon as it is ready, without asking for the visitor's permission.

&lt;audio controls autoplay&gt;

&lt;source src="http://www.learn.com/uploads/audio.mp3" type="audio/mpeg"&gt;

Audio element not supported by your browser.

&lt;/audio&gt;

loop

This attribute is used to have the audio replay everytime it's finished.

&lt;audio controls autoplay loop&gt;

&lt;source src="http://www.learn.com/uploads/audio.mp3" type="audio/mpeg"&gt;

Audio element not supported by your browser.

&lt;/audio&gt;

Currently there are three supported format for the &lt;audio&gt; element: MP3, WAV, and OGG.

## The video element

The video element is similar to the audio element.

You can specify the video source URL using an attribute in a video element, or using source elements inside the video element.

&lt;video controls&gt;

&lt;source src="http://www.learn.com/uploads/video.mp4" type="video/mp4"&gt;

&lt;source src="http://www.learn.com/uploads/video.ogg" type="video/ogg"&gt;

Video is not supported by your browser

&lt;/video&gt;

Another aspect that the audio and video elements have in common is that the major browsers do not all support the same file types. If the browser doesn't support the first video type, it will try the next one.

Another aspect shared by both audio and video elements is that each has controls, autoplay and loop attributes.

&lt;video controls autoplay loop&gt;

&lt;source src="http://www.learn.com/uploads/video.mp4" type="video/mp4"&gt;

&lt;source src="http://www.learn.com/uploads/video.ogg" type="video/ogg"&gt;

Video is not supported by your browser

&lt;/video&gt;

Currently, there are three supported video format for the video element: MP4, WebM and OGG.

## The progress element

The &lt;progress&gt; elements provide the ability to create progress bars on the web.

The progress element can be used within headings, paragraphs or anywhere in the body.

### Attributes

Value: specifies how much of the task has been completed.

Max: specifies how much work the task requires in total.

Status: &lt;progress min="0" max="100" value="35"&gt;

&lt;/progress&gt;

Use the &lt;progress&gt; tag in conjunction with JavaScript to dynamically display a tasks progress.

## Web storage API

With html5 web storage, websites can store data on a users local computer.

Before html5, we had to use JavaScript cookies to achieve this functionality.

### The advantages of web storage

More secure

Faster

Stores large amount of data

Stored data is not sent with every server request.

NB: local storage is per domain. All pages from one domain can store and access the same data.

### Types of web storage objects

There are two types of web storage objects:

sessionStorage()

localstorage()

Session storage is destroyed once the user closes the browser.

Local storage stores data with no expiration date.

You need to be familiar with JavaScript in order to understand and use the API.

### Working with values

The syntax for web storage for both local and session storage is both simple and similar.

The data is stored as key/value pairs.

Storing a value:

localStorage.setItem("key1", "value1");

Getting a value:

//this will print the value

alert(localStorage.getItem("key1"));

Removing a value:

localStorage.removeItem("key1");

Removing all values:

localStorage.clear();

The same syntax applies to the session storage with one difference : instead of localStorage, sessionStorage is used.

## Geolocation API

In html5, Geolocation API is used to obtain the users geographical location.

Since this can compromise the users privacy, the option is not available unless the user approves it.

Geolocation is much more accurate for device with GPS, like smartphones.

### Using html Geolocation

The Geolocation API's main method is getCurrentPosition, which retrievers the current geographical location of the user's device.

JS:

navigator.geolocation.getCurrentPosition();

### Parameters

showLocation(mandatory): Defines the callback method that retrieves location information.

ErrorHandler(optional): Defines the callback method that is invoked when an error occurs in processing the asynchronous call.

Options (optional): Defines a set of options for retrieving the location information.

You need to be familiar with basic JavaScript in order to understand.

### Presenting data

User location can be presented in two ways: Geodetic and civic.

1. Geodetic way to describe position refers directly to latitude and longitude.
    
2. The civic presentation of location data is presented in a format that is more easily read and understood by the average person.
    

### Attributes

Position

Elevation

Heading

Speed

Orientation

The getCurrentPosition() method returns an object if it is successful. The latitude, longitude and accuracy properties are always returned.

## Drag and Drop API

The drag and drop feature lets you "grab" an object and drop it to a different location.

To make an element draggable, just set the draggable attribute to true:

&lt;img draggable="true" /&gt;

Any element can be draggable.

The API for html5 drag and drop is event based.

&lt;!DOCTYPE HTML&gt;

&lt;html&gt;

&lt;head&gt;

&lt;script&gt;

function allowDrop(ev) {

ev.preventDefault();

}

function drag(ev) {

ev.dataTransfer.setData("text", ev.target.id);

}

function drop(ev) {

ev.preventDefault();

var data = ev.dataTransfer.getData("text");

ev.target.appendChild(document.getElementById(data));

}

&lt;/script&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;div id="box" ondrop="drop(event)"

ondragover="allowDrop(event)"

style="border:1px solid black;

width:200px; height:200px"&gt;&lt;/div&gt;

&lt;img id="image" src="sample.jpg" draggable="true"

ondragstart="drag(event)" width="150" height="50" alt="" /&gt;

&lt;/body&gt;

&lt;/html&gt;

### What to drag

When the element is dragged, the ondragstart attribute call's a function, drag(event), which specifies what data is to be dragged.

The dataTranser.setData() method sets the data type and the value of the draged data:

function drag(ev) {

ev.dataTransfer.setData("text", ev.target.id);

}

In our example, the data is "text" and the value is the ID of the draggable element ("image").

### Where to drop

The ondragover event specifies where the dragged data can be dropped. By default, data and element cannot be dropped in other elements.

To allow a drop, we must prevent the default handling of the element. This is done by calling the event.preventDefault() method for the ondragover event.

### Do the drop

When the dragged data is dropped, a drop event occurs. In the example above, the ondrop attribute calls a function, drop(event):

function drop(ev) {

ev.preventDefault();

var data = ev.dataTransfer.getData("text");

ev.target.appendChild(document.getElementById(data));

}

The preventDefault() method prevents the browser's default handling of the data (default is open as link on the drop).

The dragged data can be accessed with the dataTransfer.getData() method. This method will return any data that was set to the same type in the setData() method.

The dragged data is the ID of the element("image").

At the end the dragged element is appended into the drop element, using the appendChild() function.

Basic knowledge of JavaScript is required to understand the use of the API.

## SVG

### Drawing

SVG stands for Scalable Vector Graphics, and is used to draw shapes with html-style markup.

It offers several methods for drawing paths, boxes, circles, text and graphic images.

SVG is not pixel-based, so it can be magnified infinitely with no loss of quality.

### Inserting SVG images

An SVG image can be added to html code with just a basic image tag that includes a source attribute pointing to the image:

&lt;img src="image.svg" alt="" height="300" /&gt;

SVG defines vector-based graphics in XML format.

### Drawing a circle

To draw shapes with SVG, you first need to create an SVG element tag with two attributes: width and height:

&lt;svg width="1000" height="1000"&gt;&lt;/svg&gt;

### To create a circle add a &lt;circle&gt; tag

&lt;svg width="2000" height="2000"&gt;

&lt;circle cx="80" cy="80" r="50" fill="green" /&gt;

&lt;/svg&gt;

cx pushes the center of the circle further to the right of the screen.

cy pushes the center of the circle further down from the top of the screen.

r defines the radius

fill determines the color of our circle.

stroke adds an outline to the circle.

Every element and every attribute in SVG files can be animated.

### Other shape elements

&lt;rect&gt; defines a rectangle:

&lt;svg width="2000" height="2000"&gt;

&lt;rect width="300" height="100"

x="20" y="20" fill="green" /&gt;

&lt;/svg&gt;

&lt;line&gt; defines a line segment:

&lt;svg width="400" height="410"&gt;

&lt;line x1="10" y1="10" x2="200" y2="100"

style="stroke:#000000; stroke-linecap:round;

stroke-width:20" /&gt;

&lt;/svg&gt;

(x1,y1) define the start coordinate (x2,y2) define the end coordinate.

&lt;polyline&gt; defines the shape built for multiple line definitions:

&lt;svg width="2000" height="500"&gt;

&lt;polyline style="stroke-linejoin:miter; stroke:black;

stroke-width:12; fill: none;"

points="100 100, 150 150, 200 100" /&gt;

&lt;/svg&gt;

Points are the polyline's coordinates.

### &lt;ellipse&gt; and &lt;polygon&gt;

The &lt;ellipse&gt; is similar to the &lt;circle&gt; with one exception:

You can independently change the horizontal and vertical axes of it's radius using the rx and ry attributes.

&lt;svg height="500" width="1000"&gt;

&lt;ellipse cx="200" cy="100" rx="150" ry="70" style="fill:green" /&gt;

&lt;/svg&gt;

The &lt;polygon&gt; element is used to create a graphic with at least three sides. The polygon element is unique because it automatically closes off the shape for you.

&lt;svg width="2000" height="2000"&gt;

&lt;polygon points="100 100, 200 200, 300 0"

style="fill: green; stroke:black;" /&gt;

&lt;/svg&gt;

Polygon comes from Greek. "Poly" means "many" and "gon" means "angle".

## SVG animations and paths

### Shape animations

SVG animations can be created using the &lt;animate&gt; element.

The example below creates a rectangle that will change it's position in 3 seconds and will then repeat the animation twice:

&lt;svg width="1000" height="250"&gt;

&lt;rect width="150" height="150" fill="orange"&gt;

&lt;animate attributeName="x" from="0" to="300"

dur="3s" fill="freeze" repeatCount="2"/&gt;

&lt;/rect&gt;

&lt;/svg&gt;

attributeName: specifies which attribute will be affected by the animation.

from: specifies the starting value of the attribute.

to: specifies the ending value of the attribute.

dur: specifies how long the animation runs (duration).

fill: specifies whether or not the attribute's value should return to it's initial value when the animation is finished (Values: "remove" resets the value; "freeze" keeps the "to value")

repeatCount: specifies the repeat count of the animation.

In the example above, the rectangle changes it's x attribute from 0 to 100 in 3 seconds.

To repeat the animation indefinitely, use the value "indefinite" for the repeatCount attribute.

### Paths

The &lt;path&gt; element is used to define a path.

The following commands are available for path data :

M: moveto

L: lineto

H: horizontal lineto

V: vertical lineto

C: curveto

S: smooth curveto

Q: quadratic Bézier curve

A: elliptical Arc

Z: closepath

### Define a path using the d attribute:

&lt;svg width="500" height="500"&gt;

&lt;path d="M 0 0 L200 200 L200 0 Z" style="stroke:#000; fill:none;" /&gt;

&lt;/svg&gt;

M places our "virtual pen" at the position 0,0. It then moves 200px down and to the right, the moves up to the position 200,0. The Z command closes the shape, which results in a hypotenuse.

All of the above commands can also be expressed with lower case letters. When capital letters are used, it indicates absolute position ; lower case indicates relative position.

## Canvas

### The &lt;canvas&gt; element

The html canvas is used to draw graphics that includes everything from simple lines to complex graphic objects.

The &lt;canvas&gt; element is defined by:

&lt;canvas id="canvas1" width="200" height="100"&gt;

&lt;/canvas&gt;

The &lt;canvas&gt; element is only a container for graphics. You must use a script to actually draw the graphics (usually JavaScript).

The &lt;canvas&gt; element must have an id attribute so it can be referred to by JavaScript:

&lt;html&gt;

&lt;head&gt;&lt;/head&gt;

&lt;body&gt;

&lt;canvas id="canvas1"

width="400" height="300"&gt;&lt;/canvas&gt;

&lt;script&gt;

var can = document.getElementById("canvas1");

var ctx = can.getContext("2d");

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

getContext() returns a drawing context on the canvas.

Basic knowledge of JavaScript is required to understand and use the canvas.

### Canvas coordinates

The html canvas is a two-dimensional grid.

The upper-left corner of the canvas has the coordinates (0,0).

The canvas element is only a container for graphics.

### Drawing shapes

The fillRect(x,y,w,h) method draws a "filled" rectangle in which w indicates the width and h indicates the height. The default fill color is black.

A 100\*100 pixels rectangle is drawn on the canvas at the position (20,20)

&lt;html&gt;

&lt;head&gt;&lt;/head&gt;

&lt;body&gt;

&lt;canvas id="canvas1" width="400" height="300"&gt;

&lt;/canvas&gt;

&lt;script&gt;

var c=document.getElementById("canvas1");

var ctx=c.getContext("2d");

ctx.fillRect(20,20,100,100);

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

The fillStyle property is used to set a color, gradient or pattern to fill the drawing.

Using this property allows you to draw a green-filled rectangle.

&lt;html&gt;

&lt;head&gt;&lt;/head&gt;

&lt;body&gt;

&lt;canvas id="canvas1" width="400" height="300"&gt;

&lt;/canvas&gt;

&lt;script&gt;

var canvas=document.getElementById("canvas1");

var ctx=canvas.getContext("2d");

ctx.fillStyle ="rgba(0, 200, 0, 1)";

ctx.fillRect (36, 10, 22, 22);

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

The canvas supports various other methods for drawing:

### Draw a line

moveTo(x,y): defines the starting point of the line.

lineTo(x,y): defines the ending point of a line.

### Draw a circle

beginPath(): starts the drawing.

arc(x,y,r,start,stop): sets the parameters of the circle.

stroke(): ends the drawing.

### Gradients

createLinearGradient(x,y,x1,y1): creates a linear gradient.

createRadialGradient(x,y,r,x1,y1,r1): creates a circular gradient.

### Drawing text on the canvas

Font: defines the font property for the text.

fillText(text,x,y): draws "filled" text on the canvas.

strokeText(text,x,y): draws text on the canvas (no fill).

There are many other methods aimed at helping to draw shapes and images on the canvas.

## SVG vs Canvas

### Canvas

Elements are drawn programmatically.

Drawing is done with pixels.

Animations are not built in.

High performance for pixel-based drawing operations.

Resolution dependent.

No support for event handlers.

You can save the resulting image as .png or .jpg

Well suited for graphic- intensive games.

### SVG

Elements are part of the DOM (document object module).

Drawing is done with vectors.

Effects, such as animation are built in.

Based on standard XML syntax, which provides better accessibility.

Resolution independent.

Support for event handlers.

Not suited for game applications.

Best suited for applications with large rendering areas ( For example, Google maps).

You can actually use both canvas and svg on the same page if needed. However, you cannot just draw svg onto a canvas, or vice-versa.

## Canvas Transformations

### Working with canvas

The canvas element can be transformed.

As an example, a text is written on the canvas at the coordinates (10,30).

&lt;html&gt;

&lt;head&gt;&lt;/head&gt;

&lt;body&gt;

&lt;canvas id="canvas1" width="400" height="300"&gt;

&lt;/canvas&gt;

&lt;script&gt;

var c=document.getElementById("canvas1");

var ctx=c.getContext("2d");

ctx.font="bold 22px Tahoma";

ctx.textAlign="start";

ctx.fillText("start", 10, 30);

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

The translate(x,y) method is used to move the canvas.

X indicates how far to move the grid horizontally , and y indicates how far to move the grid vertically.

ctx.translate(100, 150);

ctx.fillText("after translate", 10, 30);

In this example, the canvas is moved 100 pixels to the right and 150 pixels down.

Canvas have several methods for drawing paths, boxes, circles, text and adding images.

## The rotate() method

The rotate() method is used to rotate the html5 canvas. The value must be in radians not degree.

Here's an example that draws a rectangle before and after rotation is set.

&lt;html&gt;

&lt;head&gt;&lt;/head&gt;

&lt;body&gt;

&lt;canvas id="canvas1" width="400" height="300"&gt;

&lt;/canvas&gt;

&lt;script&gt;

var c=document.getElementById("canvas1");

var ctx=c.getContext("2d");

ctx.fillStyle = "#FF0000";

ctx.fillRect(10,10, 100, 100);

ctx.rotate( (Math.PI / 180) \* 25); //rotate 25 degrees.

ctx.fillStyle = "#0000FF";

ctx.fillRect(10,10, 100, 100);

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

The rotation will only affect drawings made after rotation is done.

### The scale() method

The scale method scales the current drawing. It takes two parameters:

The number of times by which the image should be scaled in the x-direction.

The number of times by which the image should be scaled in the y-direction.

&lt;html&gt;

&lt;head&gt;&lt;/head&gt;

&lt;body&gt;

&lt;canvas id="canvas1" width="400" height="400"&gt;

&lt;/canvas&gt;

&lt;script&gt;

var canvas = document.getElementById('canvas1');

ctx =canvas.getContext('2d');

ctx.font="bold 22px Tahoma";

ctx.textAlign="start";

ctx.fillText("start", 10, 30);

ctx.translate(100, 150);

ctx.fillText("after translate", 0, 0);

ctx.rotate(1);

ctx.fillText("after rotate", 0, 0);

ctx.scale(1.5, 4);

ctx.fillText("after scale", 0,20);

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

If you scale a drawing, all future drawings will also be scaled.

## HTML5 Forms, Part 1

Html5 brings many features and improvements to web form creations.

There are new attributes and input types that were introduced to help create better experiences for web users.

Form creation is done in html5 the same way as it was in html4:

&lt;form&gt;

&lt;label&gt;Your name:&lt;/label&gt;

&lt;input id="user" name="username" type="text" /&gt;

&lt;/form&gt;

Use the novalidate attribute to avoid form validation on submissions.

### New attributes

Html5 has introduced a new attribute called placeholder. On &lt;input&gt; and &lt;textarea&gt; elements, this attribute provides a hint to the user of what information can be entered into the field.

&lt;form&gt;

&lt;label for="email"&gt;Your e-mail address: &lt;/label&gt;

&lt;input type="text" name="email" placeholder="email@example.com" /&gt;

&lt;/form&gt;

The autofocus attribute makes the desired input focus when the form loads:

&lt;form&gt;

&lt;label for="email"&gt;Your e-mail address: &lt;/label&gt;

&lt;input type="text" name="email" autofocus /&gt;

&lt;/form&gt;

The required attribute tells the browser that the input is required.

### Forms with required fields

&lt;form autocomplete="off"&gt;

&lt;label for="e-mail"&gt;Your e-mail address: &lt;/label&gt;

&lt;input name="Email" type="text" required /&gt;

&lt;input type="submit" value="Submit"/&gt;

&lt;/form&gt;

The form will not be submitted without filling the required fields.

The autocomplete attribute specifies whether a form or input field should have autocomplete turned on or off.

When autocomplete is on, the browser automatically complete values based on values the user has entered before.

### Html5 added several new input types

color

date

datetime

datetime -local

email

month

number

range

search

tel

time

url

week

### New input attributes in html5

autofocus

form

formaction

formenctype

formmethod

formnovalidate

formtarget

height and width

list

min and max

multiple

pattern (regexp)

placeholder

required

step

Input types that are not supported by old web browsers, will behave as input type text.

## HTML5 Forms, Part 2

### Creating a search box

The new search input type can be used to create a search box.

&lt;input id="mysearch" name="searchitem" type="search" /&gt;

You must remember to set a name for your input; otherwise, nothing will be submitted.

### Search options

The &lt;datalist&gt; tag can be used to define a list of predefined options for the search field:

&lt;input id="car" type="text" list="colors" /&gt;

&lt;datalist id="colors"&gt;

&lt;option value="Red"&gt;

&lt;option value="Green"&gt;

&lt;option value="Yellow"&gt;

&lt;/datalist&gt;

&lt;option&gt; defines the options in a drop-down list for the user to select.

The ID of the datalist element must match with the list attribute of the input box.

### Creating more fields

Some other new input types include email, url and tel:

&lt;input id="email" name="email" type="email" placeholder="example@example.com" /&gt;

&lt;br /&gt;

&lt;input id="url" name="url" type="url" placeholder="example.com" /&gt;

&lt;br /&gt;

&lt;input id="tel" name="tel" type="tel" placeholder="555.555.1211" /&gt;

These are especially useful when opening a page on the modern mobile device, which recognizes input type and opens a corresponding keyboard matching the field's type.

These new types makes it easier to structure and validate html forms.