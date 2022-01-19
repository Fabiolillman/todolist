<template>
     <ul class="list-container" id="listContainer">
      <TodoItem 
      :todo="item"
      v-for="(item,index) in todos" 
      v-bind:key="index" 
      @removeTodo="removeIndex(index)"
      @checkComplete="completeCheck"
      />
    </ul>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
 

 components: {
    TodoItem,
  },

  props: [
  'todos'
  ], 

  methods:{
    removeIndex(index){      
    this.$emit('removeItem', index)
    },

     checkComplete(){      
     this.$emit('completeCheck')
    },
  }
}
</script>

<style>

</style>