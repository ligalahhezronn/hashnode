---
title: "Forms, input and label"
datePublished: Wed Apr 10 2024 06:31:49 GMT+0000 (Coordinated Universal Time)
cuid: clutfn5mj000y08jqd8u31g5o
slug: forms-input-and-label

---

You can interact with the visitors of your website and collect information from the using forms.

You can use forms to let your visitors:

* get in contact with you.
    
* send orders, requests and other information.
    
* create an account or register.
    
* and much more
    

Forms are made of input elements like text field, checkboxs, and submit buttons. These input elements are nested inside the &lt;form&gt; container tag.

The most common form element is &lt;input&gt;.

There are many forms of &lt;input&gt; element, depending on the type of attribute.

```python
<form>
    input type text radio checkbox
</form>
```

Form elements will be displayed on the same line unless we use the &lt;br&gt; (line break) tag.

Label can be added for the different input elements with the label tag.

It's considered a very good practise to connect the label tag to the input elements with the use of for and id attributes.

```python
<form>
    <input type="text" id="one">
    <label for="one">Text</label>
</form>
```

The id attribute is used to identify a unique input element. The for attribute in a label target and matches an input's id.

Correctly connecting labels and form fields will increase hit area and improve accessibility.

When labels and form fields are correctly connected hitting the label selects the form field.