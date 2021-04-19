<template>
  <div id="card">
<div class="crd" v-on:click="onClick">
    <h3>{{ heading }}</h3>
    <p>{{ inStock }}</p>
    </div>
  </div>
</template>

<script>
export default {
name: 'Card',
props: {
    heading: String,
    inStock: String,
    onClick: {
      type: Function,
      required: true
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
</style>