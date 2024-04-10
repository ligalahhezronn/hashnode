---
title: "Lists Elements"
datePublished: Wed Apr 03 2024 19:56:17 GMT+0000 (Coordinated Universal Time)
cuid: cluk8aqq0000408lb7uvq78o3
slug: lists-elements

---

In modern web development, lists are very useful elements.

You can even use lists to build navigation menus.

A list consists of **list items** `<li>`.

* Item 1
    
* Item 2
    
* Item 3
    

List items are container tags with the list item nested inside.

```xml
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
```

**Ordered list** `<ol>` show with numbers instead of bullets.

1. Lemon
    
2. Papper
    
3. Rozeey
    

Use `<ol>` when the points have a certain order, like step-by-step instructions.

Use unordered list `<ul>` when the order of the items is not important. They are shown with bullet points.

You can nest a list inside another list.

```xml
<ol>
  <li>Fruits</li>
    <ul>
      <li>Apple</li>
      <li>Banana</li>
    </ul>
  <li>Milk</li>
  <li>Cheese</li>
</ol>
```

A list can contain any number of items.

Indentation is used to show nested elements.

```xml
<ol>
  <li>First item</li>
    <ul>
      <li>Subitem A</li>
      <li>Subitem B</li>
    </ul>
  <li>Second item</li>
</ol>
```

Remember the browser will ignore line breaks and white spaces in HTML code and each list item will be placed on a new line.

You can nest elements like list items inside hyperlinks.

**Remember:**

⭐ Lists are made of list items &lt;li&gt;

⭐ You can add ordered &lt;ol&gt; and unordered &lt;ul&gt; lists to web pages

⭐ You can nest lists inside each other

In the next article of this series, we will look at how to use attributes to modify HTML elements.