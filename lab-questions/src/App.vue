// this is the view
<template>
  <div id="app">
      <h1> Vue Lab</h1>
      <MessageBox message="This is a msg from the props (property) area in MessageBox.vue" bgcolor="orange"></MessageBox>
      <MessageBox messsage="Another color here please" v-bind:bgcolor="preferedColor"></MessageBox>
      <!-- displays whatever was in the 'text' string  -->
      <h1>{{text}}</h1>
      <!-- @ is shorthand for v-on -->
      <button @click="buttonPressed">Click</button>
      <input type="text" v-model="preferedColor"/>
      <Light></Light>
      <SayGreetings/>
      <Counter/>
      <Dice/>
      <Form/>
      <Sum/>
      <SignupForm/>
  </div>
</template>


// this is the model & controller
<script>

import MessageBox from './components/MessageBox'
import Light from './components/Light'
import SayGreetings from './components/SayGreetings'
import Counter from './components/Counter'
import Dice from './components/Dice'
import Form from './components/Form'
import Sum from './components/Sum'
import SignupForm from './components/SignupForm'


export default {
  name: 'App',
  components: {
      MessageBox, Light, SayGreetings,Counter, Dice, Form, Sum, SignupForm
  },

  data: function(){
      return {
        //   empty text string which is then filled in the buttonPressed function()
          'text': '',
          'preferedColor': 'azure',
      }
  },
  methods: {
      'buttonPressed': function(){
        //   alert("Hello World")
            //  links back to the data with the key 'text'
            this.text = "You Clicked Me!"
      }
  }
}
</script>

// this is the styling
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
