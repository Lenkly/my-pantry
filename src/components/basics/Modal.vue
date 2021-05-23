<template>
  <div id="modal" v-if="active">
    <!-- <div class="overlay" v-on:click="toggleModal"></div> -->
    <div class="modal-container">
      <div class="modal-header">
        <h3>
          {{ heading }}
        </h3>
      </div>

      <div class="modal-body">
        <p>
          {{ description }}
        </p>
      </div>

      <div class="modal-footer">
        <p>
          {{ details }}
        </p>
      </div>
      <Button v-on:click="toggleModal" text="Cool story, bro!" />
    </div>
  </div>
</template>

<script>
import Button from './Button'

export default {
  name: 'Modal',
  components: Button,
  props: {
    heading: String,
    description: String,
    details: String
  }
}
</script>

<style>
.modal-container {
  width: 80vw;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 0 5px 2px white;
  transition: all 0.3s ease;
  transform-origin: 0 0;
}

.modal-header h3 {
  margin-top: 0;
  color: #42b983;
}

.modal-body,
.modal-footer {
  margin: 20px 0;
}

.modal-body p,
.modal-footer p {
  color: #202237;
}

.overlay {
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.modal-enter-active,
.modal-leave-active {
  transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  will-change: transform, opacity;
}

.modal-leave-active {
  transition-delay: 0.35s;
}

.modal-enter,
.modal-leave-to {
  opacity: 0;
  transform: scale3d(0, 0, 0);
}
</style>
