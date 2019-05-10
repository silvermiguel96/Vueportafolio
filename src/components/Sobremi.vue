<template>
  <div class="sobreMi">
    <h2>Sobre Mi</h2>
    <p>{{ person.data[0].sobre}}</p>
  </div>
</template> 
<script>
export default { 
  props: { 
    person: {
      type: Object, required: true } 
    } 
};
</script> 
<style scoped>
.sobreMi {
  width: 80%;
  margin: 0 auto;
}
h2 {
  font-size: 2.5em;
  border-bottom: 1px solid green;
  color: green;
}
p {
  font-size: 1.5em;
  padding-top: 1em;
  margin: 0 0.8em;
}
</style>