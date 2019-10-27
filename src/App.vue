<template>
  <!-- <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div> -->
<div class="">

  <h1>Trivia</h1>
  <Questions></Questions>

</div>


</template>

<script>
import Questions from './components/Questions.vue'

export default {
  name: 'app',
  data(){
    return{
      trivia: []
    }
  },
  mounted(){
    fetch('https://opentdb.com/api.php?amount=10')
    .then(res => res.json())
    .then(trivia => this.trivia = trivia)},

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
