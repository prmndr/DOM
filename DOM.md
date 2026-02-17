<!DOCTYPE html>
<html>
<head>
    <title>Understanding DOM - Interactive Demo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f6f9;
            text-align: center;
            padding: 30px;
        }

        .box {
            background-color: white;
            padding: 20px;
            margin: 20px auto;
            width: 60%;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        button {
            padding: 10px 15px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
        }

        .btn1 { background-color: #3498db; color: white; }
        .btn2 { background-color: #2ecc71; color: white; }
        .btn3 { background-color: #e74c3c; color: white; }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            padding: 5px;
        }
    </style>
</head>

<body>

    <h1>📘 How DOM Works (Live Example)</h1>

    <div class="box">
        <h2 id="title">Hello Students!</h2>
        <p id="description">
            DOM allows JavaScript to change this content dynamically.
        </p>

        <button class="btn1" onclick="changeText()">Change Text</button>
        <button class="btn2" onclick="changeColor()">Change Color</button>
        <button class="btn3" onclick="addItem()">Add List Item</button>
    </div>

    <div class="box">
        <h3>📌 Dynamic List (DOM in Action)</h3>
        <ul id="list">
            <li>Item 1</li>
            <li>Item 2</li>
        </ul>
    </div>

<script>

    // Function 1: Change Text Content
    function changeText() {
        document.getElementById("title").innerHTML = "🎉 DOM Changed This Text!";
        document.getElementById("description").innerHTML = 
        "JavaScript accessed the DOM and modified the HTML element.";
    }

    // Function 2: Change Style (CSS using DOM)
    function changeColor() {
        document.getElementById("title").style.color = "blue";
        document.getElementById("description").style.fontSize = "18px";
    }

    // Function 3: Create and Add New Element
    function addItem() {
        let newItem = document.createElement("li");   // Create element
        newItem.innerHTML = "New Item Added by DOM";  // Add text
        
        document.getElementById("list").appendChild(newItem); // Add to list
    }

</script>

</body>
</html>
