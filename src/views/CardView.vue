<template>
  <div class="cardcontainer">
    <h1 style="margin-bottom: 30px">Beispiel-Cards</h1>
    <div id="cards">
      <Card heading="Kaffee" inStock="Das ist ein Beispieltext, lol." />
      <Card
        heading="Dr. Oetker rote Grütze Himbeere und Waldmeister hmmmmm"
        inStock="Das ist ein Beispieltext, lol."
      />
      <Card
        heading="Gewürzgurken vom Aldi"
        inStock="Das ist ein Beispieltext, lol."
      />
      <Card
        heading="Deine Mudda im Glas, voll spezial"
        inStock="Das ist ein Beispieltext, lol."
      />
      <Card heading="Puderzucker" inStock="Das ist ein Beispieltext, lol." />
      <Card heading="Tempura" inStock="Das ist ein Beispieltext, lol." />
      <Card heading="Tomatensaft" inStock="Das ist ein Beispieltext, lol." />
      <Card
        heading="Getrocknete Tomaten ohne Öl"
        inStock="Das ist ein Beispieltext, lol."
      />
      <Card
        heading="Tuc Kekse mit Paprikageschmack"
        inStock="Das ist ein Beispieltext, lol."
      />
      <Card heading="Backpulver" inStock="1 Bazillion!!!" />
      <Card
        heading="Grillgewürz aus Kanada"
        inStock="Das ist ein Beispieltext, lol."
      />
      <Card heading="Eine selbstgebackene Torte" inStock="3/4 Teil" />
      <Card
        onClick="toggleOpen"
        v-bind:class="{ 'is-open': open }"
        heading="Sriracha"
        inStock="Das ist ein Beispieltext, lol."
      />
      <transition name="modal">
        <Modal
          v-show="open"
          heading="Sriracha"
          description="Das ist ein Beispieltext, lol."
          details="2 Stück"
        />
      </transition>
    </div>
  </div>
</template>

<script>
import Card from '../components/basics/Card.vue'
import Modal from '../components/basics/Modal.vue'

export default {
  name: 'App',
  data: () => ({
    open: false
  }),
  components: {
    Card,
    Modal
  },
  methods: {
    toggleOpen() {
      this.open = !this.open
    }
  }
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
