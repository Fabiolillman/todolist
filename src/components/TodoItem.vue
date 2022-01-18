<template>
  <div class="check-box" >
  <!-- <Checkbox /> -->
    <label></label>
    <input type="checkbox" > 
    <span>{{todo.content}}</span>
    <img class="trash" src="../assets/delete.svg">
    <button @click="yell)">Test Delete</button>
    
  </div>
</template>

<script>
  export default {
  data(){return{
 
  }},
  props:[
    'todo',
  ],

  methods:{
 
  yell(){
    console.log(this.item)
  },
  
  //  deleteTodo(){      
      // this.todos = !this.todos
      // persist(this.todos)
    // },
    
 
    // checkTodo(){
    //   // this.item.done = !this.item.done

    //   this.item = this.item.filter(t => !t.done)
      // persist(this.todos)
    },
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
