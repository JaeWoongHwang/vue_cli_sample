<template>
  <div>
    <input type="text" v-model="newTodoItem">
    <button v-on:click="addTodo">추가</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: ""
    };
  },
  methods: {
    // 입력받은 텍스트 로컬 스토리지에 저장
    addTodo() {
      localStorage.setItem(this.newTodoItem, this.newTodoItem);
    }
  }
}
</script>

<style>
</style>
