<template>
  <div id="exercise">
      <!-- 1) Show an alert when the Button gets clicked -->
      <div>
          <button v-on:click="alert">Show Alert</button>
      </div>
      <!-- 2) Listen to the "keydown" event and store the value in a data property (hint: event.target.value gives you the value) -->
      <div>
          <input type="text" v-on:keyup="valueBind">
          <p>{{value}}</p>
      </div>
      <!-- 3) Adjust the example from 2) to only fire if the "key down" is the ENTER key -->
      <div>
          <input type="text" v-on:keydown.enter="valueBind">
          <p>{{value}}</p>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Exercise2',
  data: function() {
    return {
      value: ''
    }
  },
  methods: {
    alert: function () {
      alert('Button gets clicked!');
    },
    valueBind: function (event) {
    this.value = event.target.value;
    }
  }
};

</script>
