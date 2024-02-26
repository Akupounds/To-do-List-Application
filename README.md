# To-do List Application
 Build a to-do list application using HTML, CSS and JavaScript 
   <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

      <link rel="stylesheet" href="style.css">

  <script src="script.js" defer></script> <!-- Include script.js here with the defer attribute -->
  
  
    <title>My To-Do List</title>
    <style>
        /* Add script src="script.js"></script> styles here */
    </style>
</head>
<body>
  <div class="container">

    <h1>My To-do List</h1>

    <input type="text" id="taskInput" placeholder="Add a new task">
    <button onclick="addTask()">Add Task</button>

    <ul id="taskList">
        <!-- Tasks will be added here dynamically -->
    </ul>

    <script>
        function addTask() {
            var taskInput = document.getElementById("taskInput");
            var taskList = document.getElementById("taskList");

            if (taskInput.value.trim() !== "") {
                var newTask = document.createElement("li");
                newTask.textContent = taskInput.value;
                taskList.appendChild(newTask);
                taskInput.value = ""; // Clear the input field
            }
        }
    </script>

</body>
</html>
