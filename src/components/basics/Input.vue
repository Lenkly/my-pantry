<template>
  <input class="npt" type="text" placeholder="Enter name of the item" />
</template>

<script>
export default {
  name: 'Input',
  props: {
    input: String
  }
}
</script>

<style scoped>
.npt {
  border: 0.5px white solid;
  border-radius: 8px;
  padding: 10px 15px;
  background: rgba(255, 255, 255, 0.3);
  color: white;
  margin-bottom: 20px;
  max-width: 25%;
}
@media screen and (max-width: 620px) {
  .npt {
    max-width: 100%;
  }
}
</style>
