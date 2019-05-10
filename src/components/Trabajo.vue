<template>
  <section class="trabajo">
    <h2>Trabajos</h2>
    <div class="containertrabajo" v-for="p in person.data[0].jobs" :key="p.tiempo">
      <p><strong>Tiempo: </strong>{{p.tiempo}}</p>
      <p><strong>Cargo: </strong>{{p.cargo}}</p>
      <p><strong>Empresa: </strong>{{p.empresa}}</p>
    </div>
  </section>

</template>

<script>
export default {
props:{
  person: {
    type: Object , required: true
  }
}
}
</script>
<style scoped>
.trabajo {
  margin: 1em 0;
  width: 80%;
  margin: 0 auto;
}
h2 {
  margin-top: 1em;
  font-size: 2.5em;
  border-bottom: 1px solid green;
  color: green;
}
.containertrabajo {
  margin: 10px 0 10px 0;
  padding: 10px
}
p{
  font-size: 1.5em;
  margin: 0 1em;
}
</style>
