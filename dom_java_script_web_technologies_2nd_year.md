# 📘 Document Object Model (DOM)
## Subject: Web Technologies (2nd Year)

---

# 1️⃣ Introduction to DOM

The **Document Object Model (DOM)** is a programming interface for HTML and XML documents.

It allows JavaScript to:
- Access HTML elements
- Modify content
- Change styles
- Add or remove elements
- Respond to user actions (click, input, etc.)

👉 In simple words:
DOM is a bridge between **HTML** and **JavaScript**.

---

# 2️⃣ Why DOM is Needed?

Without DOM:
- Web pages would be static (no changes after loading).

With DOM:
- We can create dynamic websites.
- Content can change without refreshing the page.

Example:
- Clicking a button changes text.
- Submitting a form shows a message.

---

# 3️⃣ How DOM Works

When a web page loads:

1. Browser reads HTML
2. Browser converts HTML into a DOM tree
3. JavaScript can access and modify this tree

---

# 4️⃣ DOM Tree Structure 🌳

HTML Code Example:

```html
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello</h1>
    <p>Welcome</p>
  </body>
</html>
```

DOM Tree Representation:

                 Document
                     |
                   html
                  /    \
               head    body
                |      /   \
              title  h1     p
                |      |     |
             My Page  Hello  Welcome

👉 Each box is called a **Node**.

---

# 5️⃣ Types of DOM Nodes

1. Document Node – Entire HTML document
2. Element Node – HTML tags (<div>, <p>, <h1>)
3. Text Node – Text inside elements
4. Attribute Node – Attributes like id, class

Example:

```html
<p id="para">Hello</p>
```

- `<p>` → Element Node
- `id="para"` → Attribute Node
- `Hello` → Text Node

---

# 6️⃣ Selecting Elements in DOM

JavaScript provides methods to select elements.

1. Select by ID
```javascript
document.getElementById("idName");
```

2. Select by Class
```javascript
document.getElementsByClassName("className");
```

3. Select by Tag Name
```javascript
document.getElementsByTagName("p");
```

4. Query Selector (Modern & Powerful)
```javascript
document.querySelector("#idName");
document.querySelector(".className");
```

---

# 7️⃣ Changing Content using DOM

HTML:
```html
<p id="demo">Old Text</p>
```

JavaScript:
```javascript
document.getElementById("demo").innerHTML = "New Text";
```

👉 The text changes without refreshing the page.

---

# 8️⃣ Changing CSS using DOM

```javascript
document.getElementById("demo").style.color = "red";
document.getElementById("demo").style.fontSize = "20px";
```

Before:
Black text

After:
Red text with bigger size

---

# 9️⃣ Creating and Adding Elements

Create Element:
```javascript
let newPara = document.createElement("p");
newPara.innerHTML = "This is new paragraph";
```

Add Element:
```javascript
document.body.appendChild(newPara);
```

Flow Diagram:

JavaScript → Create Element → Add to DOM → Visible on Page

---

# 🔟 Removing Elements

```javascript
let element = document.getElementById("demo");
element.remove();
```

Element disappears from page.

---

# 1️⃣1️⃣ DOM Events

DOM allows interaction using events.

Common Events:
- onclick
- onmouseover
- onsubmit
- onkeydown

Example:

HTML:
```html
<button onclick="changeText()">Click Me</button>
```

JavaScript:
```javascript
function changeText() {
  document.getElementById("demo").innerHTML = "Button Clicked!";
}
```

Event Flow Diagram:

User Action → Event Triggered → JavaScript Function → DOM Updated

---

# 1️⃣2️⃣ Parent, Child, and Sibling Relationship

DOM follows tree structure.

Example:

<body>
  <div>
     <p>Hello</p>
  </div>
</body>

Tree View:

body
 |
 div  ← child of body
  |
  p   ← child of div

- body → parent of div
- div → parent of p
- p → child of div

Useful Properties:

```javascript
element.parentNode
element.childNodes
element.firstChild
element.lastChild
```

---

# 1️⃣3️⃣ DOM vs HTML

HTML:
- Static structure

DOM:
- Live representation in browser
- Can be modified using JavaScript

Simple Comparison:

HTML File → Browser → DOM Tree → JavaScript Controls It

---

# 1️⃣4️⃣ Real-Life Example

Imagine DOM like a family tree 👨‍👩‍👧‍👦

Grandparent (html)
   |
Parent (body)
   |
Child (div)
   |
Grandchild (p)

JavaScript can:
- Change family members
- Add new members
- Remove members
- Change their style

---

# 1️⃣5️⃣ Advantages of DOM

✅ Makes web pages interactive
✅ Allows dynamic content updates
✅ Easy manipulation of HTML & CSS
✅ Works with all modern browsers

---

# 1️⃣6️⃣ Summary

✔ DOM stands for Document Object Model
✔ It converts HTML into a tree structure
✔ JavaScript uses DOM to manipulate web pages
✔ DOM makes websites dynamic and interactive

---

# 📌 Important Exam Questions

1. Define DOM with diagram.
2. Explain DOM tree structure.
3. What are different types of DOM nodes?
4. Write JavaScript code to change content using DOM.
5. Explain DOM events with example.

---

# 🎯 Final Conclusion

The DOM is one of the most important concepts in Web Technologies.

If you understand:
- Tree structure
- Element selection
- Content modification
- Events

You can build interactive websites easily 🚀

---

End of Document

