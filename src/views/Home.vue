<template>
  <div id="app">
    <img alt="Vue logo" src="../assets/logo.jpg" />
    <Intro msg="What's in my pantry?!" name="Christian" />

    <div id="buttons">
      <Button :onClick="clickButton" text="Have a look!" />
      <Button :onClick="clickButton" text="Change User" disabled />
    </div>
  </div>
</template>

<script>
import Intro from '../components/Intro.vue'
import Button from '../components/basics/Button.vue'

export default {
  name: 'App',
  components: {
    Intro,
    Button
  },
  methods: {
    clickButton() {
      alert('my pantry is empty at the moment 🥺')
    }
  }
}
</script>

<style>
#app {
  text-align: center;
  margin: 60px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
#buttons {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
</style>
