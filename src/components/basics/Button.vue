<template>
  <button type="text" class="btn" v-on:click="onClick">{{ text }}</button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
    onClick: {
      type: Function,
      required: true
    }
  }
}
</script>

<style scoped>
.btn {
  display: inline-block;
  white-space: nowrap;
  font-size: 20px;
  border: solid 2px white;
  border-radius: 8px;
  padding: 10px 15px;
  color: white;
  background-color: #00ad8b;
  box-shadow: 0 0 5px 2px #00ad8b;
  cursor: pointer;
  margin-bottom: 20px;
  align-self: stretch;
  max-width: 350px;
  transition: all 0.5s ease;
}
@media screen and (max-width: 620px) {
  .btn {
    max-width: 100%;
  }
}
.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 2px 5px 2px #00ad8b;
}
.btn:disabled {
  opacity: 0.5;
  transform: translateY(0);
  box-shadow: 0 0 5px 2px #00ad8b;
  cursor: not-allowed;
}
</style>
