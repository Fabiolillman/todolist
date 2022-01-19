<template>
  <div class="check-box" >
  <!-- <Checkbox /> -->
    <label></label>
    <input type="checkbox" @click="checkComplete"> 
    <span>{{todo.content}}</span>
    <img @click="removeTodo" class="trash" src="../assets/delete.svg">
  
    
  </div>
</template>

<script>
  export default {
  data(){return{
 
  }},
  props:[
    'todo',
    'index',
  ],

  methods:{

   removeTodo(){      
     this.$emit('removeTodo')
    },

     checkComplete(){      
     this.$emit('checkComplete')
    },
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
span{
  font-size: 30px;

}
ul{
  display: flex;
  flex-direction: row;
  align-content: center;
}
.checkbox{
  margin-top: 20px;
}

</style>
