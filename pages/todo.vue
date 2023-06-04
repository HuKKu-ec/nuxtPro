<template>
  <h1 class="todo-head">Todo is here....!</h1>

  <div class="list-contaner">
    <div class="list" v-for="obj in objs">
      <p>{{ obj.todo }}</p>
      <p class="close" @click="($e) => closeTodos(obj)">close</p>
    </div>
  </div>
  <div class="inp">
    <input
      :value="text"
      @input="
        (event) => {
          text = event.target.value;
        }
      "
      class="text-input"
      placeholder="Enter your todos...!"
    />
    <button class="btn" @click="($e) => addTodos(text)">ADD</button>
  </div>
</template>
<script setup>
const objs = useState(() => []);
const addTodos = (text) => {
  if (text) objs.value.push({ todo: text, id: Math.random() });
};
const closeTodos = (obj) => {
  objs.value = objs.value.filter((e) => {
    return e.id != obj.id;
  });
};
</script>

<style scope>
.todo-head {
  text-align: center;
  color: #0c134f;
  margin: 50px 0px;
}
.list {
  display: flex;
  margin: 10px;
}
.list {
  background-color: #0c134f;
  padding: 30px;
  color: #fff;
}
.close {
  margin-left: auto;
  cursor: pointer;
}
.inp {
  width: 100%;
  text-align: center;
}
.text-input {
  all: unset;
  width: 50%;
  margin: 20px 2px;
  background-color: #e7e7e7;
  border-radius: 5px;
  padding: 10px;
}
</style>
