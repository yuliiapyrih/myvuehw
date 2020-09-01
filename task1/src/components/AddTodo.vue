<template>
  <div>
  <input type="text" v-model='list'>
  <button @click='save' v-show='show'>Save point</button>
  </div>
</template>

<script>
export default {
  name: 'AddTodo',
  props:{
    show:{
        type:Boolean,
        default:true
    }
  },
  data(){
    return{
      list:''
    }
  },
  methods:{
    save(){
      const value=this.list;
      this.$emit('saveItem',value)
      this.list='';
  }
  }
}
</script>


<style>

</style>
