---
title: "Submitting forms"
datePublished: Sun Apr 14 2024 19:11:10 GMT+0000 (Coordinated Universal Time)
cuid: cluzwj3cf000508la9nqy0kml
slug: submitting-forms

---

An html form is a convenient way to send data to a database hosted in a server.

A **submit** button is used to send the data in a form. The **submit** type of input adds a button to the form.

```xml
<form>
<label for="em">email:</label>
<input type="text" id="em"><br>
<input type="submit">
</form>
```

You can use the **submit** input to send the data in the form to a database hosted in a server.

The **name** attribute is used to reference the data after submitting the form.

```xml
<form>
<input type="text" name="email">
<input type="text" name="city">
<input type="submit">
</form>
```

The name attribute is used to put the input from the user in the correct **field** (column) in the database. 

The **value** attribute defines the value that is submitted when the input is selected.

```xml
<p>Enter payment option</p>
    <input type="radio" id="r1" 
    name="pay" value="cash">
    <label for="r1">Cash</label>
    <input type="radio" id="r2" 
    name="pay" value="card">
    <label for="r2">Card</label>
```

Names and values are needed to correctly store information in the database. The HTML code needs to include **where** and **what** to put in the database.