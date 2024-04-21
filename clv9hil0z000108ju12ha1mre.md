---
title: "JavaScript User Inputs"
datePublished: Sun Apr 21 2024 12:08:34 GMT+0000 (Coordinated Universal Time)
cuid: clv9hil0z000108ju12ha1mre
slug: javascript-user-inputs

---

Handling user inputs effectively will make your web page stand out.

The **confirm ()** box asks the user to accept or reject something. Similar to alert () and prompt (), the box takes the focus away from the current window and forces the user to read the message.

You can store the decision from the user in a variable and use it later in your code. A confirm () box returns **true** if the user clicks OK and **false** if the user clicks on Cancel.

In a similar way, a checkbox represents two states, selected **(true)** or deselected **(false)**.

You can use **.checked** to get the state of the checkbox.

```xml
<form id="myForm">
  <label for="c1">Tick this box</label>
  <input type="checkbox" id="c1"></br></br>
  <input type="button" onclick="checkTicked()" value="Check if Ticked"></input>
</form>
```

```css
#table {
  background-color: #525252;
  padding: 20px;
  color: white;
}

#dataTable {
  width: 60%;
  margin: 0 auto;
  border-collapse: collapse;
  color: white;
}

th, td {
  border: 1px solid #DDDDDD;
  padding: 8px;
}

th {
  background-color: #494949;
  padding-top: 12px; 
  padding-bottom: 12px; 
  text-align: left;
}

h2 {
  text-align: center;
}
```

```javascript
function checkTicked() {
  let box = document.getElementById("c1");
  console.log(box.checked);
}
```

A checkbox in a news site is used to **"Accept Terms & Conditions"**. The checkbox element has been accessed and stored in variable called **terms**.