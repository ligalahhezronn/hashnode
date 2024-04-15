---
title: "Drop-down menus"
datePublished: Mon Apr 15 2024 18:47:24 GMT+0000 (Coordinated Universal Time)
cuid: clv1b4dnq000v08jp4nuz2g65
slug: drop-down-menus

---

Drop-down menus make your forms more efficient, accessible, and organized.

You can use the **&lt;select&gt; container tag** to create a drop-down list.

The **&lt;option&gt; container tag** is used inside a &lt;select&gt; tag to add choices for the user.

You can use the **&lt;select&gt;** element as part of a form to collect user input.

Submitting a form sends information to a database. The **name** attribute is needed to submit the form data.

```xml
form>
<select name="color">
<option>Red</option>
<option>Blue</option>
</select>
</form>
```

Data will be sent when the form is submitted. You can control the data each option sends with the **value** attribute.

```xml
<select id="dropdown">
 <option value="r">Red</option>
 <option value="g">Green</option>
 <option value="b">Blue</option>
</select>
```

The **selected** attribute creates a drop-down menu with a pre-selected option. The pre-selected option will be displayed first.

```xml
<select name="color">
 <option value="r">
         Red</option>
 <option value="g">
         Green</option>
 <option value="b" selected>
         Blue</option>
</select>
```

You can add labels to drop-down menus.

```xml
<form>

<label>

Vehicle type:

</label>

<select name="vehicle">

<option value="car">Car</option>

<option value="bus">Bus</option>

</select>

</form>
```

Labels and drop-down menus are connected with **for** and **id** attributes, just like any other form element.

```xml
<form>
 <label for="s1">
      Vehicle type:</label>
  <select name="vehicle" id="s1">
   <option value="car">
      Car</option>
   <option value="bus">
      Bus</option>
  </select>
</form>
```

**&lt;input type="text"&gt;:**

**text box**

**&lt;input type="checkbox"&gt;:**

**checkbox**

**&lt;input type="radio"&gt;:**

**radio button**

**&lt;input type="submit"&gt;:**

**submit button**

There are many other types of input elements that you can use in your forms. 

```xml
<input type="email">
<input type="password">
<input type="tel">
```