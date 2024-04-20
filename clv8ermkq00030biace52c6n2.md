---
title: "Block elements, Divs, Tables"
datePublished: Sat Apr 20 2024 18:03:51 GMT+0000 (Coordinated Universal Time)
cuid: clv8ermkq00030biace52c6n2
slug: block-elements-divs-tables

---

Every html element is either inline or block.

Block elements start on a new line.

  

### Block

p

ul

### Inline

button

b

  

Format tags are inline elements

* i
    
* b
    
* u
    

  

Inline elements can be nested inside block-level elements.

Line break &lt;br&gt; tags are used to force inline elements to start on a new line.

  

# Divide and Conquer

Grouping different HTML elements can make your pages faster to load and easier to customize and maintain.

  

&lt;div&gt; takes full available width.

&lt;div&gt; is a container that groups related content on a web page, such as a sidebar or a navigation menu. &lt;div&gt; doesn’t add meaning to the content because it’s a… non semantic tag.

&lt;div&gt; doesn't add any visual effect unless you add a style to it. It’s often used by web developers to group and style HTML elements.

The style in a &lt;div&gt; container will apply to all its nested elements unless you give them their own.

Black is the default color for text.

  

# Tables

Tables help you display data in a way that’s easy to scan, compare, and analyze.

```xml
<html>

  <head>

    <title>Page Title</title>

  </head>

  <body>

    <table>

      <tr>

        <td>C1</td>

        <td>C2</td>

      </tr>

      <tr>

        <td>C3</td>

        <td>C4</td>

      </tr>

    </table>      

  </body>

</html>
```

  
Borders can be added to tables, rows and cells with the style attribute.

&lt;td&gt; elements within the same row are displayed on the same line, one after the other.

Tables usually include headers. A header is a special row at the top of the table used to label each column.

You can include several headers in HTML tables.

You can make cells that take up multiple rows and/or columns, using the attributes **colspan** and **rowspan.** This is called merging cells.

```html
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <table style="border:solid">
      <tr>
        <th style="border:solid">Month</th>
        <th style="border:solid">
		Budget($)</th>
      </tr>
      <tr>
        <td style="border:solid">
		January</td>
        <td style="border:solid">
		500</td>
      </tr>
      <tr>
        <td style="border:solid">
		February</td>
        <td style="border:solid">400</td>
      </tr>
      <tr>
        <td style="border:solid"
        colspan="2">Sum: 900</td>
      </tr>
    </table>    	
  </body>
</html>
```

The **rowspan** attribute specifies the number of rows a cell should span. You can use rowspan to merge cells vertically.