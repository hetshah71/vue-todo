<template>
    <div class="todo-list-container">
        <div class="todo-list">
            <div v-for="(todo, index) in todos" :key="index" class="todo-item">
                <input type="checkbox" v-model="todo.completed" class="todo-checkbox" />
                <span :class="{ completed: todo.completed }" class="todo-text">{{ todo.text }}</span>
                <div class="todo-actions">
                    <button class="edit-button" @click="editTodo(index)">
                        <span class="edit-icon">✏️</span>
                    </button>
                    <button class="delete-button" @click="deleteTodo(index)">
                        <span class="delete-icon">🗑️</span>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue'
const todos = ref([
    { text: 'Study', completed: false },
    { text: 'Playing', completed: false },
])

</script>

<style lang="scss" scoped>
.todo-list-container {
  background-color: white;
  padding: 15px;
  margin-bottom: 15px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  flex: 1;
  overflow: hidden; /* Remove scrolling */
  width: 100%;
  display: flex;
  flex-direction: column;
}

.todo-list {
  margin-top: 0;

  .todo-item {
    display: flex;
    align-items: center;
    padding: 12px;
    background-color: white;
    border-bottom: 1px solid #e2e8f0;
    margin-bottom: 0;
    transition: all 0.2s ease;

    .todo-checkbox {
      width: 20px;
      height: 20px;
      margin-right: 15px;
      cursor: pointer;
      accent-color: #4299e1;
    }

    .todo-text {
      flex: 1;
      font-size: 1rem;
      color: #2d3748;

      &.completed {
        text-decoration: line-through;
        color: #a0aec0;
      }
    }
    
    .todo-actions {
      display: flex;
      gap: 5px;
    }

    button {
      width: 30px;
      height: 30px;
      border: none;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: background-color 0.2s ease;

      &.edit-button {
        background-color: #ff9500;
        color: white;

        &:hover {
          background-color: #e68600;
        }
      }

      &.delete-button {
        background-color: #ff3b30;
        color: white;

        &:hover {
          background-color: #e6352b;
        }
      }
      
      .edit-icon, .delete-icon {
        font-size: 14px;
      }
    }
  }
}
</style>