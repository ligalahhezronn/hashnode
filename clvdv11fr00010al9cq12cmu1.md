---
title: "Font styles"
datePublished: Wed Apr 24 2024 13:37:55 GMT+0000 (Coordinated Universal Time)
cuid: clvdv11fr00010al9cq12cmu1
slug: font-styles

---

Fonts play a crucial role in web design, influencing readability, aesthetics, and user experience. They breathe life to the words of the page and set tone of the content.

The **font-family** in CSS lets you specify the typeface for your text.

Georgia

Arial

Courier New

Comic Sans MS

Lucida Console

Tahoma

Many fonts are installed by default in all devices. These are known as **web safe** fonts.

  
Other fonts might need to be installed on the user’s device, so you’ll need to specify a web safe font as a back-up, in case the user doesn’t have them.

The font-family property specifies a list of fonts, from highest priority to lowest. Font selection stops at the first font in the list that is on the user's system.

![img-component](https://lecontent.sololearn.com/material-images/760a347d4c814400bc4a3e7edaec86bc-23.png align="left")

Generic font families are groups of fonts with similar typefaces, and they are used as universal fallbacks. It's a best practice to place them as the last option in a font-family property. If the preferred fonts are unavailable, browsers will use a font from that family.

Use **quotes** to wrap font names with multiple words. It's good practice. 

The font-weight property controls the thickness (or boldness) of the text.

You can use numerical values from **100** (thinnest) to **900** (thickest) to specify font weight, increasing in **increments of 100.**

Certain weight values, such as 400 and 700, have named equivalents that can be used directly as values: normal and bold.