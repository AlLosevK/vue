<template>
  <div id="exercise">
    <!-- 1) Fill the <p> below with your Name and Age - using Interpolation -->
    <p>VueJS is pretty cool - {{name}}, {{age}}
      <span v-if='age!=0'>years.</span>
    </p>
    <!-- 2) Output your age, multiplied by 3 -->
    <p v-if="age!=0">{{ age*3 }}</p>
    <!-- 3) Call a function to output a random float between 0 and 1 (Math.random()) -->
    <p v-once>{{ RandomFloat () }}</p>
    <!-- 4) Search any image on Google and output it here by binding the "src" attribute -->
    <div>
      <img v-bind:src="imageLink" style="width:100px;height:100px">
    </div>
    <!-- 5) Pre-Populate this input with your name (set the "value" attribute) -->
    <div>
      <input type="text" v-model="name">
      <input type="text" v-model="age">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Exercise1',
  data: function() {
    return {
      name: '(NAME)',
      age: '(AGE)',
      imageLink: 'https://012.vuejs.org/images/logo.png'
    }
  },
  methods: {
    RandomFloat: function () {
      return Math.random()
    }
  }
};
</script>
