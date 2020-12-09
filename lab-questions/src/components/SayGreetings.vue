<template>
  <div>
    <h1>{{text}}</h1>
    <button @click="buttonPressed1">Say Hi</button>
    <button @click="buttonPressed2">Say Goodbye</button>
    <button @click="buttonPressed3">Sleep</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      //   empty text string which is then filled in the buttonPressed function()
      text: "",
    };
  },
  methods: {
    buttonPressed1: function () {
      //  links back to the data with the key 'text'
      this.text = "Hello World";
    },
    buttonPressed2: function () {
      //  links back to the data with the key 'text'
      this.text = "Goodbye World";
    },
    buttonPressed3: function () {
      //  links back to the data with the key 'text'
      this.text = "zzz...zzz...zzz";
    },
  },
};
</script>

<style scoped>
</style>