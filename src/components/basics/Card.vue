<template>
  <div id="card">
<div class="crd" v-on:click="showModal = true">
    <h3>{{ heading }}</h3>
    <p>{{ inStock }}</p>
    </div>
    <transition>
      <div class="modal-overlay" 
         v-if="showModal" 
         v-on:close-modal="showModal = false"></div>
    </transition>
    <transition name="pop" appear>
    <div class="modal" 
         role="dialog" 
         v-if="showModal"
         >
      <h1>Vue Transitions</h1>
      <p>The <code>&lt;transition&gt;</code> component in Vue can create wonderful animated entrances and exits.</p>
      <button v-on:click="closeModal()" class="button">Hide Modal</button>

    </div>
  </transition>
  </div>
</template>

<script>

import Modal from './Modal'

export default {
name: 'Card',
components: Modal,
props: {
    heading: String,
    inStock: String
},
data() {
    return {
      modal: false
    };
  },
methods : {
        closeModal() {
            this.$emit('closeModal');
        }
    }
}
</script>

<style scoped>
.crd {
    display: inline-block;
    padding: 10px 15px;
    border: white solid 2px;
    border-radius: 8px;
    box-shadow: 0 0 5px 3px #00AD8B;
    background-color: rgba(255, 255, 255, 0.3);
    margin-bottom: 20px;
    width: 264px;
}
.crd:hover {
  transform: translateY(-2px); 
  background-color: rgba(255, 255, 255, 0.5);
  box-shadow: 0 3px 5px 3px #00AD8B;
}
/* @media screen and (min-width: 568px) {
  .crd {
    margin-right: 20px;
  }
} */
h3 {
    display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;  
  overflow: hidden;
}
p {
font-size: 14px;
font-weight: 200;
}

.modal {
  position: absolute;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  text-align: center;
  width: fit-content;
  height: fit-content;
  max-width: 22em;
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.2);
  background: #FFF;
  z-index: 999;
  transform: none;
}
.modal h1 {
  margin: 0 0 1rem;
}

.modal-overlay {
  content: '';
  position: absolute;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 998;
  background: #2c3e50;
  opacity: 0.6;
  cursor: pointer;
}

/* ---------------------------------- */
.fade-enter-active,
.fade-leave-active {
  transition: opacity .4s linear;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.pop-enter-active,
.pop-leave-active {
  transition: transform 0.4s cubic-bezier(0.5, 0, 0.5, 1), opacity 0.4s linear;
}

.pop-enter,
.pop-leave-to {
  opacity: 0;
  transform: scale(0.3) translateY(-50%);
}
</style>