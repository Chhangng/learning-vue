<script>
     export default{
       data(){
          return {
            contact :" 12345 Test",
            Atr : 'title',
            input1 :'style1',
            count : 0,
            text: ''
          }
       },
       methods:{
           tom()
           {
               this.count++
           },
           toj(){
               this.count--
           }
       }
    }

</script>

<template>
        <h1 v-bind:id="Atr">{{contact.split( '').reverse('').join( '')}}</h1>
        <button v-on:click="tom"> Click me :{{ count }}</button>
        <button v-on:click="toj"> Click me :{{ count }}</button> <br> <br>
        <input v-model="text"  placeholder="please input"> 
        <p  :id="input1">{{ text }}</p>

</template>

<style>
    #title{
      color: red;
      height: 100px;
      width: 100px;
      background-color: aqua;
      padding: 12px;
      font-size: 12px;
      line-height: 80px;
      text-align: center;
    }
    #style1{
      color: rgb(132, 21, 84);
    }
</style>