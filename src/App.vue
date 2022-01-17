<template>
  <div id="app">
    <div class="menu-container">
    <Menu />
    </div>
    <div class="top-container">
   <img src="./assets/teflon-panna.svg">
   <h1>TEFLON</h1>
   <p>När det inte fastnar</p>
   <p class="top-p-row">Du har {{numberLeft}} todos kvar att göra</p>
   </div>
   <ul class="list-container">
   <TodoList :listName="listName"/>
   </ul>
   <div class="btn-container">
   <input type="text" v-model="listName">
   <button @click='printNames'>Lägg till todo</button>
   </div>
  </div>
</template>



<script>
import TodoList from './components/TodoList.vue'
import Menu from './components/Menu.vue'
export default {

   methods:{
    printNames(){
      this.printName = this.listName
    }
  },

  name: 'App',
  components: {
    TodoList,
    Menu
  },

  data(){return{
    listName:''
  }}
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
