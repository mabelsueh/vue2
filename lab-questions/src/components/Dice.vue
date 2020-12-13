<template>
  <div>
    <div class="container dice" v-if="number % 2 == 0">
      <div v-if="number == 6">
        <p v-bind:style="{ color: 'green' }">{{ number }}!</p>
      </div>
      <div v-else>
        <p>{{ number }}!</p>
      </div>
      <br />
    </div>
    <div class="container dice" v-else>
      <div v-if="number == 1">
        <p v-bind:style="{ color: 'red' }">{{ number }}</p>
      </div>
      <div v-else>
        <p>{{ number }}</p>
      </div>
      <br />
    </div>
    <br />
    <button @click="randomize">Roll Dice</button>
    <br /><br />
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
  width: 100px;
  height: 100px;
  border: 1px solid black;
}
.even {
  color: black;
}
</style>