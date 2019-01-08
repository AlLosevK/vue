<template>
  <div id="exercise">

    <!-- 1) Start the Effect with the Button. The Effect should alternate the "highlight" or "shrink" class on each new setInterval tick (attach respective class to the div with id "effect" below) -->
    <div>
      <button @click="startEffect">Start Effect</button>
      <div id="effect" :class="{highlight: classSwitcher, shrink: !classSwitcher}"></div>
    </div>

    <!-- 2) Create a couple of CSS classes and attach them via the array syntax -->
    <div>I got no class :(</div>

    <!-- 3) Let the user enter a class (create some example classes) and attach it -->
    <div>
      <input type="text" v-model="inputClass">
      <div :class="inputClass">Choose highlight(or)shrink</div>
    </div>

    <!-- 4) Let the user enter a class and enter true/ false for another class (create some example classes) and attach the classes -->
    <div>
      <input type="text" v-model="rotateClass">
      <input type="text" v-model="upDown" v-on:keydown.enter="setNormalClass(upDown)">
      <div class="centr"
      :class="[rotateClass, normalClass]">Put class in first input, and set true/false for second by enter</div>
    </div>

    <!-- 5) Repeat 3) but now with values for styles (instead of class names). Attach the respective styles.  -->
    <div>
      <input type="text">
      <div></div>
    </div>

    <!-- 6) Create a simple progress bar with setInterval and style bindings. Start it by hitting the below button. -->
    <div>
      <button v-on:click="startProgress">Start Progress</button>
      <div class="progressBar" :class="progressBarValue"></div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Exercise4',
  data: function() {
    return {
      classSwitcher: false,
      inputClass: '',
      rotateClass: 'centr',
      normalClass: '',
      upDown: 'false',
      progressBarValue: 'progressBar'
    }
  },
  methods: {
    startEffect: function() {
      this.classSwitcher = !this.classSwitcher;
    },
    setNormalClass: function(upDown){
      if (upDown) {
        this.normalClass = 'left-right';
      } else {
        this.normalClass = 'none'
      };
    },
    startProgress: function(){
      var vm = this;
      var a = 0;
      setInterval(function(){
        a == 125 ? vm.progressBarValue = progressBarValue : vm.progressBarValue = 'progressBar' + a;
        a += 25
      },1000)
    }
  }
};
</script>

<style>
#effect {
  width: 100px;
  height: 100px;
  border: 1px solid black;
}

.centr{
  background-color: green;
  font-size: 30px;
}

.left-right{
  transform: rotate(0deg) !important;
}

.left{
  transform: rotate(-45deg);
}

.right{
  transform: rotate(45deg);
}

.centr.left,
.centr.right,
.centr.left-right{
  transition: all 1s;
}


.highlight {
  background-color: red;
  width: 200px !important;
  color: blue;
  font-size: 20px
}

.shrink {
  background-color: gray;
  width: 50px !important;
}

.progressBar {
  width: 300px;
  height: 20px;
  border: 1px solid black;
}

.progressBar0{
  background: linear-gradient(to right, red 0%, transparent 25%, transparent 50%, transparent 75%, transparent 100%);
}
.progressBar25{
  background: linear-gradient(to right, red 0%, red 25%, transparent 50%, transparent 75%, transparent 100%);
}
.progressBar50{
  background: linear-gradient(to right, red 0%, red 25%, red 50%, transparent 75%, transparent 100%);
}
.progressBar75{
  background: linear-gradient(to right, red 0%, red 25%, red 50%, red 75%, transparent 100%);
}
.progressBar100{
  background: linear-gradient(to right, red 0%, red 25%, red 50%, red 75%, red 100%);
}

</style>
