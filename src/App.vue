<template>
  <div id="app">
    <div class="menu-container">
      <Menu />
    </div>
    <div class="top-container">
      <img src="./assets/teflon-panna.svg">
      <h1>TEFLON</h1>
      <p>När det inte fastnar</p>
      <p class="top-p-row">Du har <!--{{numberLeft}} --> todos kvar att göra</p>
    </div>
    <ul class="list-container" id="listContainer">
      <TodoItem 
      :todo="item"
      v-for="item in todos" 
      v-bind:key="item.id" />
    </ul>
    <div class="btn-container">
      <input type="text" v-model="content" placeholder="type stuff here">
      <button @click='printList'>Lägg till todo</button>
      <span>{{console()}}</span>
    </div>
  </div>
</template>

<script>
import TodoItem from './components/TodoItem.vue'
import Menu from './components/Menu.vue'
export default {
  name:'app',
  
  components: {
    TodoItem,
    Menu
  },

  data(){return{

    id: '',
    content: '',
    // hideCompletedTodos: false,
    todos: [],
    
  }},
  
  methods:{
    printList(){
       this.todos.push({
         id: this.generateID(),
         content: this.content,
         done: true,
      });
      
    },
    console(){
     console.log(this.todos)
     },
    
    generateID(){
    return Math.floor(Math.random()*Math.pow(10,25))  
    },
     
  },
}
</script>













<style>
*{
  padding: 0;
  margin: 0;
}
body{
  display: flex;
  justify-content: center; 
  background: black;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 60%;
  height: 53rem;
  background: whitesmoke;
}
.menu-container{
  height: 5%;
}
.top-container{
  height: 30%;
}

h1{
  font-size: 3rem;
  margin: 0.5rem;
}
.top-p-row{
  margin-top: 5rem;
}

img{
  width: 100px;
  background-size: cover;
}

.list-container{
  height: 50%;
  background-color: white;
}

button{
  height: 50px;
  width: 300px;
  background-color: black;
  color: white;
  font-weight: 900;
  font-size: 20px;
}
input{
   height: 50px;
  width: 300px;
}
.btn-container{
  height: 15%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

</style>
