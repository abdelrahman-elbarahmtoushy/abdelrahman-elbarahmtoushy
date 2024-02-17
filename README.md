- 👋 Hi, I’m @abdelrahman-elbarahmtoushy
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
abdelrahman-elbarahmtoushy/abdelrahman-elbarahmtoushy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
function addTask() {
    var taskInput = document.getElementById('taskInput');
    var taskList = document.getElementById('taskList');

    if (taskInput.value.trim() === '') {
        alert('Please enter a task.');
        return;
    }

    var newTask = document.createElement('li');
    newTask.innerHTML = `
        ${taskInput.value}
        <button onclick="removeTask(this)">Remove</button>
    `;

    taskList.appendChild(newTask);
    taskInput.value = '';
}

function removeTask(button) {
    var taskItem = button.parentNode;
    taskItem.parentNode.removeChild(taskItem);
}
