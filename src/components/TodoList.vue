<template>
  <div class="check-box">
  <Checkbox />
  <label printname></label>
    <input type="checkbox" v-model:> 
    <span>{{printName}}</span>
  
  </div>
</template>

<script>
export default {
  data(){return{
  printName: ''
  }},
  props:[
    'listName',
    
  ],

  methods:{
    // printNames(){
    //   this.printName = this.listName
    // }
  }
}
</script>

<style scoped>

</style>
