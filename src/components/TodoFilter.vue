<template>
    <div class="filter-container">
        <div class="filter-wrapper">
            <label for="todo-filter" class="filter-label">Filter</label>
            <div class="select-wrapper">
                <select id="todo-filter" v-model="filter" class="todo-filter">
                    <option value="all">All</option>
                    <option value="active">Active</option>
                    <option value="completed">Completed</option>
                </select>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.filter-container {
  background-color: white;
  padding: 15px;
  margin-bottom: 15px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  width: 100%;
}

.filter-wrapper {
  display: flex;
  align-items: center;
}

.filter-label {
  margin-right: 10px;
  font-weight: 500;
  color: #4a5568;
}

.select-wrapper {
  position: relative;
  flex: 1;
}

.todo-filter {
  width: 100%;
  padding: 8px 12px;
  border: 1px solid #e2e8f0;
  border-radius: 4px;
  background-color: white;
  font-size: 1rem;
  color: #4a5568;
  appearance: none;
  cursor: pointer;
  
  &:focus {
    outline: none;
    border-color: #4299e1;
  }
}

.select-wrapper::after {
  content: '';
  position: absolute;
  right: 12px;
  top: 50%;
  transform: translateY(-50%);
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid #4a5568;
  pointer-events: none;
}
</style>