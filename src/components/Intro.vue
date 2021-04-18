<template>
  <div class="intro">
    <h1>{{ msg }}</h1>
    <p>
      <span style="font-weight: 700">{{ name === 'Christian' ? 'Christian' : `${name}` }}</span>, please look into the pantry list first before you buy the 30th package of baking soda.
    </p>
    <h3>Let's start!</h3>
    
  </div>
</template>

<script>
export default {
  name: 'Intro',
  props: {
    msg: String,
    name: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 25px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
