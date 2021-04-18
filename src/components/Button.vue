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
  white-space:nowrap;
  font-size: 20px;
  border: solid 2px white;
  border-radius: 8px;
  padding: 10px 15px;
  color: white;
  background-color: #00AD8B;
  box-shadow: 0 0 0 1px #00AD8B;
  cursor: pointer;
  margin-bottom: 20px;
  max-width: 25%;
}
@media screen and (max-width: 620px) {
  .btn {
    max-width: 100%;
  }
}
.btn:hover {
  transform: translateY(-2px); 
}
.btn:disabled {
  opacity: 0.5;
  transform: translateY(0);
  cursor: not-allowed;
}
</style>