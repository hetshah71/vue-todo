<template>
  <div class="todo-item">
    <input 
      type="checkbox" 
      :checked="todo.completed" 
      class="todo-checkbox" 
      @change="toggleComplete"
    />
    <span class="todo-text" :class="{ completed: todo.completed }">
      {{ todo.text }}
    </span>
    <div class="todo-actions">
      <button class="edit-button" @click="editTodo">
        <span class="edit-icon">✏️</span>
      </button>
      <button class="delete-button" @click="deleteTodo">
        <span class="delete-icon">🗑️</span>
      </button>
    </div>
  </div>
</template>

<script setup>

</script>
<style scoped>
.todo-item {
  display: flex;
  align-items: center;
  padding: 12px 15px;
  border-bottom: 1px solid #eee;
  background-color: white;
}

.todo-checkbox {
  margin-right: 10px;
}

.todo-text {
  flex-grow: 1;
}

.completed {
  text-decoration: line-through;
  color: #999;
}

.todo-actions {
  display: flex;
}

.edit-button, .delete-button {
  border: none;
  border-radius: 50%;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-left: 5px;
  cursor: pointer;
}

.edit-button {
  background-color: #f39c12;
  color: white;
}

.delete-button {
  background-color: #e74c3c;
  color: white;
}

.edit-icon, .delete-icon {
  font-size: 0.9rem;
}
</style>