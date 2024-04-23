---
title: "Write Less CSS by Taking Advantage of Inheritance"
datePublished: Tue Apr 23 2024 15:02:53 GMT+0000 (Coordinated Universal Time)
cuid: clvcimgro00050al63zpsc6aa
slug: write-less-css-by-taking-advantage-of-inheritance

---

Not every property is inherited but it tends to be anything that is typography related.

```css
body {
    margin: 0;
    font-family: 'PT Serif';
    line-hight: 1.6;
}

h1{
    font-family: "Cinzel", serif;
}
```

margin: 0; gets rid of the extra-spacing that we have by default.

The body is a good place to come in and set things like your font-family.

By default, the line-height is a little tight. It is 1.4 by default, so you might want to come up with a 1.6 or a 1.7.

When things are inherited, you don't have to worry about specificity or order or anything like that because when something is inherited it is not directly applied to it.

Putting h1 before the body won't override anything because you are still selecting h1 specifically.

One of the good things about inheritance is that it is very easy to override.

**margin-block** is a margin top and bottom.

Links, buttons and other form elements

**a** has a user agent stylesheet, color: -webkit-link; This simply means that it is coming from the user agent stylesheet, so it is the default from the browser, but they are applying a color to it. And they are also applying the cursor: pointer; which turns it into the hand-icon when you hover on a link. We also have a text-decoration: underline; So, these are styles that are coming from the browser, and we aren't inheriting anymore.

Apply whatever style you want, and it will override your user agent style.

Buttons and input don't inherit anything.

In HTML and CSS, the inheritance of styles is a fundamental concept, but not all properties are inherited by default. Text-related properties like font-size, color, and line-height are typically inherited by child elements from their parent elements, but properties like padding, margin, and border are not.

Buttons and input fields are considered replaced elements in HTML, meaning their content and appearance are determined by the user agent (such as the browser) rather than the CSS styles. Because of this, they often don't inherit styles like other HTML elements because their styles are often controlled by the browser's default stylesheet or the developer's stylesheet specifically targeting these elements.

However, you can still apply styles to buttons and inputs using CSS. You can target them directly with CSS selectors and apply styles like color, background-color, font-size, etc. Additionally, you can use pseudo-elements and pseudo-classes to style different states of buttons and inputs (such as hover, focus, etc.).

```css
button,
input,
textarea,
select {
    font: inherit;
}
```

You can set anything you want to inherit and bring them in.

It is good to use this techniques with other elements too for stuff like border-radius where we have a nested child. Just so they match all the time. This can come in handy with pseudo elements.

```css
html {
    font-size: 2rem;
}
```

By setting font-size to your html, you have basically changed what your rem is! Not advisable and it can cause a bit of havoc.