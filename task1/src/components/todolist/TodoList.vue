<template>
  <div>
    <ul>
      <li v-for="(point, indexList) in todolist" :key='indexList'>
        <TodoItem 
        :point="point"
        :indexList="indexList"
        @removeItem="removeItem"
        />
      </li>
    </ul>
    
  </div>
</template>

<script>

import TodoItem from '@/components/todolist/TodoItem.vue'

export default {
  name: 'TodoList',

  components: {
    TodoItem
  },

    props:{
        todolist:{
            type:Array,
            required: true,
            default:null
        }
    },
    data(){
        return{
        }
    },
    methods:{
        removeItem(event){
            this.$emit('removeIndex',event)
        }
    }
}
</script>


<style scoped>

</style>