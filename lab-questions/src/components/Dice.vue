<template>
  <div>
    <div class="container dice">
      {{ number }}<span class="even" v-if="number%2==0">!</span>
    </div>
    <br>
    <button @click="randomize">Roll Dice</button>
    <br><br>
  </div>
</template>

<script>
export default {
  data: function () {
    return { number: 1 };
  },
  methods: {
    randomize: function () {
      console.log((this.number = Math.floor(Math.random() * 6) + 1));
    },
  },
};
</script>

<style scoped>
.dice {
  display: flex;
  justify-content: center;
  align-items: center;
  color: red;
  width: 100px;
  height: 100px;
  border: 1px solid black;
}
.even {
    color: black;
}
</style>