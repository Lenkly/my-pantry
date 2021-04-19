<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.jpg">
    <Intro msg="What's in my pantry?!" name="Christian"/>

  <div id="buttons">
    <Button :onClick="clickButton" text="Have a look!" />
    <Button :onClick="clickButton" text="Change User" disabled />
    </div>
      <h1 style="margin-bottom: 30px">Beispiel-Cards</h1>
    <div id="cards">
<Card heading="Kaffee" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Dr. Oetker rote Grütze Himbeere und Waldmeister hmmmmm" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Gewürzgurken vom Aldi" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Deine Mudda im Glas, voll spezial" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Puderzucker" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Tempura" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Tomatensaft" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Getrocknete Tomaten ohne Öl" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Tuc Kekse mit Paprikageschmack" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Backpulver" inStock="1 Bazillion!!!" :onClick="clickCard" />
<Card heading="Grillgewürz aus Kanada" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
<Card heading="Eine selbstgebackene Torte" inStock="3/4 Teil" :onClick="clickCard" />
<Card heading="Sriracha" inStock="Das ist ein Beispieltext, lol." :onClick="clickCard" />
  </div>
  </div>
</template>

<script>
import Intro from './components/Intro.vue'
import Button from './components/basics/Button.vue'
import Card from './components/basics/Card.vue'

export default {
  name: 'App',
  components: {
    Intro,
    Button,
    Card
  },
  methods: {
    clickButton() {
      alert('my pantry is empty at the moment 🥺')
    },
    clickCard() {
      alert('not available in your country')
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
#cards {
  -moz-column-count: 4;
  -webkit-column-count: 4;
  column-count: 4;
  -moz-column-gap: 20px;
  -webkit-column-gap: 20px;
  column-gap: 20px;
}
</style>
