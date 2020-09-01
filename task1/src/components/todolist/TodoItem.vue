<template>
  <div>
    <span>{{point}}</span>
    <button @click='remove'>Delete point</button>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props:{
      point:{
          type:String,
          default:"NOOt"
      },
      indexList:{
          type:Number,
          default:null
      }
  },
  methods:{
      remove(){
          this.$emit("removeItem",this.indexList)
      }
      
  }
}
</script>

