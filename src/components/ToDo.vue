<template>
    <div>
        <input v-model="inputValue">
        <button @click="handleSubmit">提交</button>
        <ul>
            <item v-for="(item, index) of list" :key="index" :item="item" :index="index" @delete="handleDelete"></item>
        </ul>
    </div>
</template>
<script>
import todoList from './ToDoList'

export default {
  data () {
    return {
      inputValue: '',
      list: []
    }
  },
  components: {
    item: todoList
  },
  methods: {
    handleSubmit: function () {
      this.list.push(this.inputValue)
      this.inputValue = ''
    },
    handleDelete: function (index) {
      this.list.splice(index, 1)
    }
  }
}
</script>
