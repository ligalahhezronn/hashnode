---
title: "Menus and Navigation"
datePublished: Mon Apr 08 2024 17:44:44 GMT+0000 (Coordinated Universal Time)
cuid: clur8stpo000o08l9667m1fsg
slug: menus-and-navigation

---

The way visitors navigate a website depends on its design.

Websites come in two shapes:

1. Multiple-page website
    
2. Single-page website
    

The way visitors navigate your website has a big impact on user experience, search engine rankings, and therefore even sales.

The `<nav>` container tag contains a set of links that allows the user to navigate between pages of a website.

Links to the different pages are added with the anchor tag `<a>` and nested inside the `<nav>` container tag.

The html project for a multi-page website is made of different html documents.

HTML documents must be saved with the right file extensions for the web browser to recognize them.

```xml
<nav>
       <a href="index.html">Home</a>
       <a href="about.html">About</a>
       <a href="contact.html">Contact</a>
</nav> 
```

It’s best practice to name your homepage **index.html** so that the web browser can find and load it.

To jump to a specific part of a single-page website, first you need to mark the section with the **id** (ID) attribute.

```xml
<section id="footer">footer</section>
```

The **id** attribute is used to identify the element you want to target with the navigation link. 

Each id attribute value must be:

* unique
    
* within quotes
    

Once the element you want to jump to has been marked with an id, you can target it with an anchor tag &lt;a&gt;

```xml
<nav>
    <a href="#footer">footer</a>
</nav>
```

The hash character (**#**) is needed to tell the web browser that we are targeting a section of the same page.

Single page vs. multi-page website design is one of the first decisions you need to make for a new website project. Both options have their pros and cons.