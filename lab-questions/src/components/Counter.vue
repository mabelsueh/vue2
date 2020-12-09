<template>
  <div>
    <div class="container counter">
      {{ count }}
    </div>
    <div>
      <span v-if="count % 2 == 0" style="margin-left: 10px">Even</span>
      <span v-else style="margin-left: 10px">Odd</span>
    </div>
    <button @click="increase">Increase by 1</button>
    <button @click="decrease">Decrease by 1</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return { count: 0 };
  },
  methods: {
    increase: function () {
      this.count += 1;
    },
    decrease: function () {
      this.count--;
    },
  },
};
</script>

<style scoped>
.counter {
  display: flex;
  justify-content: center;
  align-items: center;
  color: blue;
  width: 100px;
  height: 100px;
  border: 1px solid black;
}
</style>