---
title: "The Undeniable Utility of CSS :has"
datePublished: Tue Sep 10 2024 04:42:42 GMT+0000 (Coordinated Universal Time)
cuid: cm0vy45uz002x09kx9oqx80qj
slug: the-undeniable-utility-of-css-has

---

I don’t know if you have noticed that CSS world has been on fire recently. All major browser vendors and the CSS specification authors have been working together to deliver tons of highly requested CSS features. Things like container queries, native CSS nesting, relative color syntax, balanced text…

One of the new features is the **:has** pseudo class.

This post is intended for developers who are already comfortable with the fundamentals of CSS, but no prior experience with :has is expected.

Parts of this post are specifically written for fellow JavaScript developers who use a framework like React/Vue/Angular, but this post should still be very useful even if you have never written any JavaScript.

# The Basics

Historically CSS selectors have worked on a “top down” fashion.

For example, by separating multiple selectors with a space, we can selectively style a child based on its parent:

```xml
<style>
 /*
    Style all <a> tags that are
    contained within <p> tags:
 */
  p a {
    font-weight: bold;
    color: inherit;
    text-decoration-color: hotpink;
    text-decoration-thickness: 2px;
  }
</style>
<p>
  This paragraph includes <a href="/">an anchor tag, commonly known as a 
  “link”</a>. Using the child combinator, we’re applying styles to anchor 
  tags when they’re included in a paragraph.
</p>
<p>
  By contrast, these links aren’t in a paragraph, so they don't get the same 
  styles:
</p>
<footer>
  <ul>
    <li>
      <a href="/">Home</a>
    </li>
    <li>
      <a href="/">About</a>
    </li>
    <li>
      <a href="/">Contact</a>
    </li>
  </ul>
</footer>
```

 The :has pseudo-selector works in a “bottom up” fashion; it allows us to style a parent based on its children:

```xml
<style>
  /*
    Style all <p> tags that contain
    at least 1 <a> tag:
  */
  p:has(a) {
    outline: 4px dashed hotpink;
    outline-offset: 4px;
    border-radius: 1px;
  }
</style>
<p>
  This paragraph includes <a href="/">an anchor tag, commonly known as a 
  “link”</a>. As a result, it is given a dashed outline.
</p>
<p>
  By contrast, this paragraph does not contain a link, and so it does not 
  receive an outline.
</p>
```

This might not seem like a big deal but it opens so many interesting new doors.

# Browser Support

Before we get to all the cool demos, we should briefly talk about browser support. **:has** is supported in all 4 major browsers starting from:

* Safari 15.4, introduced March 2022
    
* Chrome/Edge 105, introduced in August 2022
    
* Firefox 69, introduced in December 2023
    

Currently, September 10, 2024, **:has** is at ~92% browser support.

Honestly, 92% is not great when it comes to browser support… Fortunately, most of the use cases, **:has** are optional “nice-to-have” bonuses, so it is not really a big deal if they do not show up to everyone. And in other cases, we can use feature detection to provide fallback CSS.

## Feature detection

The @supports at-rule allows us to apply CSS conditionally, based on whether or not it is supported by the user’s browser.  

```xml
p {
  /* Fallback styles here */
}
@supports selector(p:has(a)) {
  p:has(a) {
    /* Fancy modern styles here */
  }
}
```

If the selector passed to the **selector ()** function is not understood by the current browser, everything within is ignored. And if the user’s browser is even older and does not recognize the @supports at-rule, the whole block is ignored. Either way, it works out.

Now, the thing is, there is no way to “mimic” **:has** using older CSS. Our fallback style will not really be able to produce the same effect. Instead, we should think of it has having two states of styles that accomplish the same goal in different ways.

# Styling based on states

```xml
<div class="card">
  <p>
    I'm
    <button>188cm</button>
    tall.
  </p>
</div>
```

In the past, I might solve this by making the whole card container a &lt;button&gt;, but this is not a good idea. Cramming so much stuff into a button would introduce several usability and accessibility issues; for example users cannot click-and-drag to select text inside the buttons!

Fortunately, we can keep our nice semantic markup and accomplish our goals with :has:

```xml
.card:has(button:focus-visible) {
  outline: 2px solid var(--color-primary);
}
/* Remove the default button focus outline */
.card button {
  outline: none;
}
```

When .card contains a focused button, we add an outline to it. The outline is applied to the parent .card, rather than to the button itself.

If you’re not familiar with the **:focus-visible** pseudo-class, it works exactly like **:focus**, but it only applies when the browser detects that the user is using the keyboard (or another non-pointer device) to navigate. When a mouse-wielding user focuses the button by clicking it, **:focus-visible** won’t be triggered, and no focus outline will be shown.

I'm also removing the default focus outline from the button, to prevent double focus indicators. **This is something we should be very cautious about.** In fact, our solution isn’t yet complete, since we also need to provide a fallback experience for folks using older browsers.

```xml
@supports selector(:has(*)) {
  .card:has(button:focus-visible) {
    outline: 2px solid var(--color-primary);
  }
  .bento-card button {
    outline: none;
  }
}
```

In this updated version, the outline modifications will only be applied for folks who visit using modern browsers. If someone is using a legacy browser, none of this stuff will apply, and they’ll see the standard focus outlines. Even though it’s a little funky, I think it’s a reasonable fallback experience.

I'm also taking a little shortcut here: rather than test for the specific selector I'm using (`.card:has(button:focus-visible)`), I'm instead using the smallest valid **:has** selector, :has(\*). The browser won't actually try and resolve the selector we supply, so it doesn’t matter which elements are selected. @supports works by looking at the syntax and establishing whether it's valid or not.

## Why not use :focus-within?

:focus-within is a pseudo-class that selects an element which contains a focused descendant. It allows us to do something quite similar;

```xml
.card:focus-within {
    outline: 2px solid var(--color-primary);
}
```

The :focus-within pseudo-class has been around much longer than :has, and so it has significantly better browser support. Seems like a better approach, no?

There are two reasons why I prefer .has in this situation:

1. :focus-within matches the :focus state, not the :focus-visible state. This means that the outline will show even for users who click the button using a mouse. There is no :focus-visible-within.
    
2. We do not want to show the focus outline when any descendant is focused, we only want it to apply when a button is focused. Some of the cards contain focusable links.
    

If we used :focus-within, it would not be clear to the user which interactive child is actually focused.

Ultimately, :focus-within can be useful but we have much finer control using :has.