<template>
  <div class="check-box" >
  <!-- <Checkbox /> -->
    <label></label>
    <input type="checkbox" > 
    <span>{{todo.content}}</span>
    <img class="trash" src="../assets/delete.svg">
    <button v-on:click='onDestroyClick'>Test Delete</button>
    
  </div>
</template>

<script>
  export default {
  data(){return{
  // printName: ''
  }},
  props:[
    'todo',
  ],

  methods:{
 
  yell(){
    console.log(this.item)
  },

  
  onDestroyClick: function(){
    // this.$destroy();
    // this.$delete(this.todo.content);
    this.todoItem=!this.todoItem
  }
   


  }
}
</script>

<style scoped>
.check-box{
  width: 100%;
  border: 2px solid black;
  margin: 1px;
  background-color: whitesmoke;

}
.trash{
width: 30px;
height: 60px;
}

</style>
