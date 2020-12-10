<template>
    <div >
       <div class="container counter">
        <div v-if="count%2==0">
            <h1 v-bind:style="{'color':'green'}">{{count}}</h1>
       </div>

         <div v-else>
            <h1 v-bind:style="{'color':'red'}">{{count}}</h1>
       </div>
       </div>

    <!-- <div>
      for the text only, not numbers (lab 2.1)
      <span v-if="count % 2 == 0" style="margin-left: 10px">{{count}}</span>
      <span v-else style="margin-left: 10px">Odd</span>
    </div> -->
    <div>
    <button @click="increase">Increase by 1</button>
    <button @click="decrease">Decrease by 1</button>
    </div>

    </div>
</template>

<script>
export default {
  data: function () {
    return { count: 0 };
  },
  //   for the buttons only
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