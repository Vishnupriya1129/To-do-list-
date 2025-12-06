# To-do list 
<!DOCTYPE html>
<html>
<head>
  <title>To-Do List Popup Edit</title>
  <style>
    body { font-family: Arial; background: #f4f4f4; display: flex; justify-content: center; align-items: center; height: 100vh; }
    .container { background: white; padding: 20px; border-radius: 10px; width: 340px; box-shadow: 0 4px 15px rgba(0,0,0,0.15); }
    h2 { text-align: center; margin-bottom: 15px; }
    input { padding: 8px; border: 1px solid #ccc; border-radius: 5px; }
    #taskInput { width: 70%; }
    #addBtn { padding: 8px 12px; margin-left: 5px; cursor: pointer; border-radius: 5px; border: none; background: #4CAF50; color: white; }
    ul { list-style: none; padding: 0; margin-top: 15px; }
    li { background: #f9f9f9; margin: 8px 0; padding: 8px; border-radius: 5px; display: flex; align-items: center; justify-content: space-between; }
    li span { flex: 1; margin-left: 10px; }
    .done { text-decoration: line-through; color: gray; }
    button { margin-left: 5px; padding: 4px 8px; border-radius: 5px; border: none; cursor: pointer; }
    .removeBtn { background: #ff4d4d; color: white; }
    .editBtn { background: #ffa500; color: white; }
    .modal { display: none; position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.6); justify-content: center; align-items: center; }
    .modal.show { display: flex; }
    .modal-content { background: white; padding: 20px; border-radius: 8px; width: 300px; text-align: center; }
    .modal-content input { width: 90%; margin-bottom: 10px; padding: 6px; }
    .saveBtn { background: #4CAF50; color: white; }
    .cancelBtn { background: #ccc; }
  </style>
</head>
<body>
  <div class="container">
    <h2>✅ To-Do List</h2>
    <input type="text" id="taskInput" placeholder="Enter task">
    <button id="addBtn">Add</button>
    <ul id="taskList"></ul>
  </div>

  <!-- Popup Modal -->
  <div class="modal" id="editModal">
    <div class="modal-content">
      <h3>Edit Task</h3>
      <input type="text" id="editInput">
      <br>
      <button class="saveBtn" id="saveEditBtn">Save</button>
      <button class="cancelBtn" id="cancelEditBtn">Cancel</button>
    </div>
  </div>

  <script>
    const taskInput = document.getElementById("taskInput");
    const addBtn = document.getElementById("addBtn");
    const taskList = document.getElementById("taskList");

    const editModal = document.getElementById("editModal");
    const editInput = document.getElementById("editInput");
    const saveEditBtn = document.getElementById("saveEditBtn");
    const cancelEditBtn = document.getElementById("cancelEditBtn");

    let tasks = JSON.parse(localStorage.getItem("tasks")) || [];
    let editIndex = null;

    function saveTasks() {
      localStorage.setItem("tasks", JSON.stringify(tasks));
    }

    function renderTasks() {
      taskList.innerHTML = "";
      tasks.forEach((task, index) => {
        const li = document.createElement("li");

        const checkbox = document.createElement("input");
        checkbox.type = "checkbox";
        checkbox.checked = task.done;
        checkbox.addEventListener("change", () => {
          tasks[index].done = checkbox.checked;
          saveTasks();
          renderTasks();
        });

        const span = document.createElement("span");
        span.textContent = task.text;
        if(task.done) span.classList.add("done");

        const editBtn = document.createElement("button");
        editBtn.textContent = "✏️";
        editBtn.className = "editBtn";
        editBtn.addEventListener("click", () => {
          editIndex = index;
          editInput.value = task.text;
          editModal.classList.add("show");
          editInput.focus();
        });

        const removeBtn = document.createElement("button");
        removeBtn.textContent = "❌";
        removeBtn.className = "removeBtn";
        removeBtn.addEventListener("click", () => {
          tasks.splice(index, 1);
          saveTasks();
          renderTasks();
        });

        li.appendChild(checkbox);
        li.appendChild(span);
        li.appendChild(editBtn);
        li.appendChild(removeBtn);
        taskList.appendChild(li);
      });
    }

    addBtn.addEventListener("click", () => {
      const text = taskInput.value.trim();
      if(text === "") return;
      tasks.push({ text, done: false });
      saveTasks();
      renderTasks();
      taskInput.value = "";
    });

    taskInput.addEventListener("keypress", e => {
      if(e.key === "Enter") addBtn.click();
    });

    saveEditBtn.addEventListener("click", () => {
      if(editIndex !== null) {
        tasks[editIndex].text = editInput.value.trim();
        saveTasks();
        renderTasks();
        editModal.classList.remove("show");
      }
    });

    cancelEditBtn.addEventListener("click", () => {
      editModal.classList.remove("show");
    });

    // Optional: close modal if click outside content
    editModal.addEventListener("click", e => {
      if(e.target === editModal) editModal.classList.remove("show");
    });

    renderTasks();
  </script>
</body>
</html>
