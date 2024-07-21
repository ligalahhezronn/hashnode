---
title: "The JavaScript substitution for IF with AND (&&) operator"
datePublished: Sun Jul 21 2024 12:45:20 GMT+0000 (Coordinated Universal Time)
cuid: clyvjwdyd00010amg3xz949l2
slug: the-javascript-substitution-for-if-with-and-operator

---

The && operator unique to JavaScript.  
With it you can quickly go from this

```javascript
function visitSite(user) {
    if (user.isLoggodIn) {
        console.log(`You are $ {user.name}`) 
    }
    console.log (“Welcome”);
}
```

  
  

To this:

```javascript
function visitSite(user) {
    user.isLoggodIn && console.log(`You are ${user.name}`);
    console.log(‘Welcome’);
}
```