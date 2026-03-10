# Ex03 To-Do List using JavaScript
## Date: 10.03.2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```html
<!DOCTYPE html>
<html>
<head>
<title>To Do List</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<div class="container">
<h2>My To Do List</h2>

<input type="text" id="taskInput" placeholder="Enter a task">
<button onclick="addTask()">Add</button>

<ul id="taskList"></ul>

</div>

<script src="script.js"></script>

</body>
</html>
```
```css
body{
font-family: Arial;
background-color: #f2f2f2;
text-align: center;
}

.container{
width: 300px;
margin: auto;
background: white;
padding: 20px;
border-radius: 10px;
box-shadow: 0px 0px 10px gray;
}

input{
width: 70%;
padding: 8px;
}

button{
padding: 8px;
background: green;
color: white;
border: none;
cursor: pointer;
}

li{
list-style: none;
padding: 8px;
margin-top: 5px;
background: #eee;
display: flex;
justify-content: space-between;
}

.delete{
background: red;
color: white;
border: none;
cursor: pointer;
}
```
```js
function addTask(){

let input = document.getElementById("taskInput");
let task = input.value;

if(task === ""){
alert("Please enter a task");
return;
}

let li = document.createElement("li");
li.textContent = task;

let deleteBtn = document.createElement("button");
deleteBtn.textContent = "Delete";
deleteBtn.className = "delete";

deleteBtn.onclick = function(){
li.remove();
};

li.appendChild(deleteBtn);

document.getElementById("taskList").appendChild(li);

input.value = "";

}
```


## OUTPUT
<img width="1920" height="1020" alt="Screenshot 2026-03-10 161843" src="https://github.com/user-attachments/assets/8ee5cf6a-36b1-4531-894f-3ca7321d05d8" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
