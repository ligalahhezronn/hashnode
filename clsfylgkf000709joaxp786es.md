---
title: "CSS Transitions and Transforms"
seoTitle: "CSS transitions and transforms "
seoDescription: "CSS transitions and transforms "
datePublished: Sat Feb 10 2024 10:54:12 GMT+0000 (Coordinated Universal Time)
cuid: clsfylgkf000709joaxp786es
slug: css-transitions-and-transforms
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1707562380348/e01c5e43-966e-4de5-9784-5c9e85cfff79.jpeg
tags: css, programming

---

## Transforms

Visual effects like moving elements makes your page more interesting.

Transformations are usually triggered by user actions. **transform**: **translate** repositions an element horizontally and / or vertically.

Providing 1 single value moves the element horizontally.

Transformations are not permanent changes. They are used to create visual effects.

When **translate** is used with 2 values, the visual effect moves the element both horizontally and vertically.

Positive values translate an element to the right and down. Negative values translate an element to the left and up.

#card:active {

transform: translate(-25px, 50px);

}

**transform**: **scale** makes an element bigger or smaller, preserving it's aspect ratio.

The original size has a value 1, so a value of 2 will double the width and height. 0.5 will halve them.

.yellow:active {

transform: scale(0.7);

}

You can rotate elements with **transform**: **rotate**;

div:active {

/\* rotates the card by

15 degrees when pressed \*/

transform: rotate(15deg);

}

Negative values results in counter-clockwise rotation.

By default, rotation takes place around the center of the element. Use **transform**\-**origin** to change the point of rotation.

transform-origin requires the horizontal and vertical position of the new point of reference.

.card:active {

transform: rotate(30deg);

/\*sets the point at

top left corner\*/

transform-origin: top left;

}

You can apply a combination of transformations to an element.

div:active {

transform: translate(100px, 150px)

rotate(70deg) scale(1.5);

}

## Transitions

Modern websites feature animated elements that captivate, guide and even affect the behavior of users.

Pseudo selectors are important when creating transitions for animations.

An **animation** produces visual effects of change in HTML elements.

**CSS** **transitions** are changes in element properties that happen over a period of time. They can be applied to a wide variety of properties and elements.

A transition requires at least: a **property** (that will change), it's **initial** **value**, a **duration** and a **trigger**.

p {

font-size: x-large;

color: white;

width: 40%;

background-color: blueviolet;

transition: width 3s;

}

p:active {

width: 100%;

}

You can change multiple properties at once in a transition. Make sure each set of instructions is separated by commas.

Use **transition**\-**delay** to add a waiting time before the transition effect.

transition-delay: 2s;

You can add transitions to Transformations.

## Keyframes & Animations

Transitions are used to produce simple animations. A transition has an initial value and a final value.

Animations are used to produce more complex animations with more intermediate states. With animations you can change as many properties as you need, as many times as you need.

Animations need **keyframes** to hold the styles that the elements will have at certain times.

element2 {

width: 150px;

height: 150px;

background-color: red;

margin: 20px;

animation-name: colorChange;

animation-duration: 3s;

}

@keyframes colorChange {

0% {

background-color: red;

}

50% {

background-color: yellow;

}

100% {

background-color: blue;

}

}

An animation is a sequence of transition.

Keyframes are snapshots with the important intermediate state that define an animation.

A new animation needs to be given an **animation**\-**name**. Use @**keyframes** followed by animation-name to define the intermediate states.

div {

width: 150px;

height: 150px;

position: relative;

margin: 50px;

animation-name: snakeMove;

animation-duration: 5s;

}

@keyframes snakeMove {

0% {

background-color: #7B41EA;

bottom: 0;

left: 0;

}

33% {

background-color: #CCB4FB;

bottom: 40px;

left: 40px;

}

66% {

background-color: #C833FD;

bottom: 0;

left: 80px;

}

100% {

background-color: #F91583;

bottom: 40px;

left: 120px;

}

}

**animation**\-**duration** controls the time it takes for the element to move from the first Keyframe to the final one.

By default, animation starts playing automatically when the page is loaded in the browser unless a delay has been set.

animation-delay adds a waiting time for the animation to start playing.

div {

padding: 30px;

border-radius: 50%;

width: 50px;

background-color: #007BFF;

color: white;

animation-name: colorChange;

animation-duration: 4s;

animation-delay: 2s;

}

@keyframes colorChange {

0% {background-color: #007BFF;}

25% {background-color: #FFC107;}

50% {background-color: #28A745;}

75% {background-color: #DC3545;}

100% {background-color: #6610F2;}

}

As an alternative to using percentages for Keyframes, you can use **from** and **to** keywords when there are only two frames for the animation.

@keyframes colorChange {

from { background-color: #007BFF;}

to { background-color: #F2106E;}

}

You can animate transformations.

To animate transformations add them to the Keyframes.

keyframes pulse {

0% { transform: scale(1);}

50% { transform: scale(2);}

100% { transform: scale(1);}

}

## Animation Properties

Transitions between 2 Keyframes are smooth and calculated automatically based on the speed function.

The default speed function is **ease**.

The ease speed function speeds up first, then slows down.

You can set alternatives to the default speed function with the **animation**\-**timing**\-**function** which can take the value, **linear**, **ease**\-**in** and **ease**\-**out** speed functions.

The **animation**\-**iteration**\-**count** property determines the number of times an animation repeats.

.circle-green {

width: 100px;

height: 100px;

top: 120px;

left: 30px;

background-color: #10FF14;

border-radius: 50%;

position: absolute;

animation: pulse 3s;

animation-iteration-count: 5;

}

To make the animation repeat forever, just use the **infinite** value with-animation-iteration-count.

The animation property can be used as a shorthand for all animation-related properties.

1. animation-name
    
2. animation-duration
    
3. animation-timing-function
    
4. animation-delay
    
5. animation-iteration-count
    

animation: spin 1s linear 0.5s infinite;

The order in which each property is declared in the shorthand declaration is important and cannot be altered, otherwise the animation will not work properly.