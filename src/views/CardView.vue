<template>
  <div class="cardcontainer">
    <h1 style="margin-bottom: 30px">Beispiel-Cards</h1>
    <div id="cards">
<Card heading="Kaffee" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Dr. Oetker rote Grütze Himbeere und Waldmeister hmmmmm" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Gewürzgurken vom Aldi" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Deine Mudda im Glas, voll spezial" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Puderzucker" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Tempura" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Tomatensaft" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Getrocknete Tomaten ohne Öl" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Tuc Kekse mit Paprikageschmack" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Backpulver" inStock="1 Bazillion!!!" />
<Card heading="Grillgewürz aus Kanada" inStock="Das ist ein Beispieltext, lol." />
<Card heading="Eine selbstgebackene Torte" inStock="3/4 Teil" />
<Card heading="Sriracha" inStock="Das ist ein Beispieltext, lol." />
  </div>
  </div>
</template>

<script>
import Card from '../components/basics/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
}
</script>

<style>
#cards {
  -moz-column-count: 4;
  -webkit-column-count: 4;
  column-count: 4;
  -moz-column-gap: 20px;
  -webkit-column-gap: 20px;
  column-gap: 20px;
}

  
</style>