<template>
  <div class="check-box">
  <Checkbox />
  <label printname></label>
    <input type="checkbox" v-model:> 
    <span >{{printedName}}</span>
  
  </div>
</template>

<script>
export default {
  data(){return{
  printName: ''
  }},
  props:[
    'inputName',
    'printedName',
    
  ],

  methods:{
    // printNames(){
    //   // this.$emit(this.printName = this.inputName)
    // }
  }
}
</script>

<style scoped>

</style>
