<template>
    <div class="todo-input-container">
        <form @submit.prevent="addTodo">
            <div class="input-wrapper">
                <input type="text" id="todo" v-model="todo" placeholder="Enter Todo here" autofocus autocomplete="off" class="new-todo" />
                <button type="submit" class="add-todo">+</button>
            </div>
        </form>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const todo = ref('');

const addTodo = () => {
  if (todo.value.trim()) {
    // Add todo logic would go here
    todo.value = '';
  }
};
</script>

<style lang="scss" scoped>
.todo-input-container {
  background-color: white;
  border-radius: 4px;
  padding: 15px;
  margin-bottom: 15px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  width: 100%;
}

form {
  margin: 0;
  width: 100%;
}

.input-wrapper {
  display: flex;
  align-items: center;
  width: 100%;
}

.new-todo {
  flex: 1;
  padding: 10px 15px;
  border: 1px solid #e2e8f0;
  border-radius: 4px;
  font-size: 1rem;
  transition: border-color 0.3s ease;
  height: 40px;

  &:focus {
    outline: none;
    border-color: #4299e1;
  }

  &::placeholder {
    color: #a0aec0;
  }
}

.add-todo {
  width: 40px;
  height: 40px;
  margin-left: 10px;
  background-color: #4299e1;
  color: white;
  border: none;
  border-radius: 50%;
  font-size: 20px;
  font-weight: 600;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  padding: 0;
  line-height: 1;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #3182ce;
  }

  &:active {
    background-color: #2b6cb0;
  }
}
</style>