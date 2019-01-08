<template>
  <div id="app">
    <HelloWorld msg="НахуюНамотано"/>
    <Exercise1/>
    <Exercise2/>
    <Exercise3/>
    <Exercise4/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Exercise1 from './components/Exercise1.vue'
import Exercise2 from './components/Exercise2.vue'
import Exercise3 from './components/Exercise3.vue'
import Exercise4 from './components/Exercise4.vue'


export default {
  name: 'app',
  components: {
    HelloWorld,
    Exercise1,
    Exercise2,
    Exercise3,
    Exercise4
  }
}
</script>

<style>
#app {
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  -webkit-flex-direction: row;
  -ms-flex-direction: row;
  flex-direction: row;
  justify-content: flex-start;
  -ms-align-items: flex-start;
  align-items: flex-start;
  -webkit-flex-wrap: wrap;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
}

#app > * {
  border: 5px solid black;
  padding: 20px 50px;
  margin: 10px
}
</style>
