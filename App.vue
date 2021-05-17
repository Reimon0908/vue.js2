<template>
  <div id="app">
    <p>合計金額：{{totalprice}}円 (税抜き)</p>
    <p>合計金額: {{totalpricetax}}円 (税込み)</p>
    
  </div>
  
</template>

<script>


export default {
  data(){
     return{
       apple:{
        name:"りんご",
        price:200
       },
       orange:{
         name:"みかん",
         price:100
       }
     };
  },
  computed:{
    totalprice(){
      return this.apple.price + this.orange.price;
    },
    totalpricetax(){
      return this.totalprice * 1.1;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2082e4;
  margin-top: 60px;
}
</style>
