<template>
  <div>
    <h1>{{text}}</h1>
    <button @click="sayHello">Say Hi</button>
    <button @click="sayGoodbye">Say Goodbye</button>
    <button @click="sayZzz">Sleep</button>
    <br><br>
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
    sayHello: function () {
      //  links back to the data with the key 'text'
      this.text = "Hello World";
    },
    sayGoodbye: function () {
      //  links back to the data with the key 'text'
      this.text = "Goodbye World";
    },
    sayZzz: function () {
      //  links back to the data with the key 'text'
      this.text = "zzz...zzz...zzz";
    },
  },
};
</script>

<style scoped>
</style>