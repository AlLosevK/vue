<template>
  <div id="app">
    <div class="">

      <button type="button" name="button"
      @click="show = !show">
        <span v-if="!show">Показать</span>
        <span v-if="show">Скрыть</span> пример 1</button>
      <HelloWorld v-if="show" msg="Не намотано"/>
    </div>

    <div class="">
      <button type="button" name="button"
      @click="show2 = !show2">
        <span v-if="!show2">Показать</span>
        <span v-if="show2">Скрыть</span> пример 2</button>
      <Exercise1 v-if="show2"/>
    </div>
    <div class="">
      <button type="button" name="button"
      @click="show3 = !show3">
        <span v-if="!show3">Показать</span>
        <span v-if="show3">Скрыть</span> пример 3</button>
      <Exercise2 v-if="show3"/>
    </div>
    <div class="">
      <button type="button" name="button"
      @click="show4 = !show4">
        <span v-if="!show4">Показать</span>
        <span v-if="show4">Скрыть</span> пример 4</button>
      <Exercise3 v-if="show4"/>
    </div>
    <div class="">
      <button type="button" name="button"
      @click="show5 = !show5">
        <span v-if="!show5">Показать</span>
        <span v-if="show5">Скрыть</span> пример 5</button>
      <Exercise4 v-if="show5"/>
    </div>
    <div class="">
      <button type="button" name="button"
      @click="show6 = !show6">
        <span v-if="!show6">Показать</span>
        <span v-if="show6">Скрыть</span> пример 5</button>
      <Exercise5 v-if="show6"/>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Exercise1 from './components/Exercise1.vue'
import Exercise2 from './components/Exercise2.vue'
import Exercise3 from './components/Exercise3.vue'
import Exercise4 from './components/Exercise4.vue'
import Exercise5 from './components/Exercise5.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Exercise1,
    Exercise2,
    Exercise3,
    Exercise4,
    Exercise5
  },
  data: function(){
    return {
      show: false,
      show2: false,
      show3: false,
      show4: false,
      show5: false,
      show6: false
  }
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

#app > div {
  border: 5px solid black;
  padding: 20px 50px;
  margin: 10px
}
</style>
