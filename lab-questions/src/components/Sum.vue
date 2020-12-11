<template>
  <div>
    <div>
      <label>Number 1: </label>
      <input type="number" v-model="num1" />
      <br /><br />
    </div>
    <div>
      <label>Number 2: </label>
      <input type="number" v-model="num2" />
      <br /><br />
    </div>
      <button @click="num3">Sum</button>
      <br>
      <span>The sum is: {{ result}}</span>
      <br><br>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      num1: 0,
      num2: 0,
      result: 0,
    };
  },
  methods: {
    num3: function () {
      this.result = parseInt(this.num1) + parseInt(this.num2);
    },
  },
};
</script>
