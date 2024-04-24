---
title: "Styling text"
datePublished: Wed Apr 24 2024 13:17:50 GMT+0000 (Coordinated Universal Time)
cuid: clvdub7go000208m90vle144i
slug: styling-text

---

Another really important element of web design is text styling.

### text-align: center;

### text-align: left;

### text-align: right;

Use **text-align: justify** to align text to both the left and right edges by adjusting the spacing between words, ensuring that each line has equal width.

Text justification is often seen in books, magazines and newspapers, as it gives neat edges to the columns of text.

You can add **text-decoration** to convey meaning or draw attention to specific pieces of text, like links.

### underline

### overline

### line-through

### underline overline

Some CSS properties can take **multiple values**. You can control the color for the decoration by adding a color name, rgb, or hex code after the decoration type..article-title { text-decoration: underline #FF4500; font-size: 24px; }

Text decoration can take on various styles, such as dotted, double, dashed, and wavy.

The text-decoration property is a short and simple way to refer to different sub-properties, such as **text-decoration-line**, **text-decoration-color**, and **text-decoration-style**.

The **text-transform** property allows you to control the capitalization of text content.

It can take 3 values: **capitalize**, **uppercase** and **lowercase**.

The **text-shadow** creates a depth effect, gives emphasis, or just adds a stylish touch to your typography.

It takes two required values, in the given order: horizontal offset first, vertical offset second.

text-shadow: horizontal-offset vertical-offset;

The **horizontal offset** is how far to the right (positive values) or left (negative values) the shadow will be.

The **vertical offse**t is how far down (positive values) or up (negative values) the shadow will be.

The text-shadow can accept two additional, optional values.

* **blur radius**: the amount of blur applied to the shadow
    
* **color:** the color of the shadow
    

```css
h1 {
  color: #FFFFFF; /* white colored text */
  text-shadow: 4px 4px 4px #4296CE; 
  font-size: 4rem;
}
```

The blur radius and color values are **optional** and can be omitted.

**text-align** controls the horizontal alignment of text.

**text-decoration** adds decorative effects to text.

**text-transform** alters the capitalization of text.

**text-shadow** applies shadow effects behind the text.