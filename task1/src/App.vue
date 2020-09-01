<template>
  <div>
    <AddTodo
    :show="show"
    @saveItem="saveItem"
    />
    <TodoList 
    :todolist="todolist"
    @removeIndex="removeIndex"
    />
  </div>
</template>

<script>

import AddTodo from '@/components/AddTodo.vue'
import TodoList from '@/components/todolist/TodoList.vue'

export default {
  name: 'App',

  components: {
    AddTodo,
    TodoList
  },

  data(){
    return{
      todolist:[],
      show:true
    }  
  },
  methods:{
    saveItem(event){
        this.todolist.push(event);
        this.todolist.length>9 ? this.show=false : this.show=true;
      },
      removeIndex(event){
        this.todolist.splice(event,1);
        this.todolist.length>9 ? this.show=false : this.show=true;
      }
  }
}
</script>

<style>

</style>
