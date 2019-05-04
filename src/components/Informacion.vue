<template>
  <section class="informacion">
    <h1> {{ person.data[0].nombre.nombre | capitalize }} {{ person.data[0].nombre.apellido | capitalize}} </h1>
    <h2> {{ person.data[0].area }}</h2>
    <h2> {{ person.data[0].location.departamento }} {{ person.data[0].location.pais }}</h2>
  </section>
</template>
<script >
export default {
  props : {
    person: {
    type: Object ,
    required: true
    }
  },
  data () {
    return {
    }
  },
  filters:{
    capitalize: function (value) {
      value = value.toString()
      return value.charAt(0).toUpperCase() + value.slice(1)
    }

  }
}
</script>
<style scoped>
.informacion {
   display: flex;
   align-items: center;
   flex-direction: column;
   margin: 50px;
}

h1 {
  font-size: 3em;
  margin: 0.3em;
}
h2 {
  font-size: 2em;
  margin: 0.2em;
}
</style>
