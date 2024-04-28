---
title: "Styling Lists"
datePublished: Sun Apr 28 2024 11:26:25 GMT+0000 (Coordinated Universal Time)
cuid: clvjg3bzx000h09k04e7n5m7c
slug: styling-lists

---

By default, unordered list items are marked with round bullets (disc).

The **list-style** property requires 3 values. It's a short and simple way to refer to 3 different sub-properties: **type**, **position** and **image**.

```css
ul{
    list-style: square inside none;
}
```

The **list-style-type** sub-property modifies the marker for both unordered and ordered lists. Let's have a look at unordered lists first

* disc
    
* none
    
* circle
    
* square
    

By default, the items in ordered list are marked with numbers.

For ordered lists, the **list-style-type** property has various possible values.

* decimal
    
* decimal-leading-zero
    
* lower-roman
    
* upper-roman
    
* lower-alpha
    
* upper-alpha
    

It's technically possible to style an ordered list with bullets and an unordered list with numbers, but it's not semantically correct and may confuse users and search engines.

Let's look at the position of markers. The **list-style-position** property accepts two possible values: **inside** and **outside**.

The default value for the position markers is outside.

The value for the list-style-image property is a URL enclosed in quotes following the **url** keyword. It specifies the path to an image file that will be used as the marker for list items.

The default value for the list-style-image property is none.