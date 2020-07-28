<template>
  <div class="hello contenedor">
    <h2>Lista de cosas por aprender</h2>
    <br>
    <h5 v-if="esVisible">Front End</h5>
    <ul class="list-group" v-for="(tech, indice) in itemsTech" v-bind:key="indice">
      <li class="list-group-item">{{ tech }}</li>
    </ul>
    <br>
    <h5 v-if="esVisible">Marketing</h5>
    <ul class="list-group" v-for="(tema, indice) in itemsMarketing" v-bind:key="indice">
      <li class="list-group-item" v-if=" indice%2 === 0 ">{{ tema }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MiLista",
  props: {},
  data: function() {
    return {
      esVisible: true,
      itemsTech: ["HTML", "CSS", "Vue", "Webpack"],
      itemsMarketing: [
        "Marketing digital",
        "Heramientas de edición",
        "Embudo de ventas",
        "Crear una Marca",
        "Estrategias de venta"
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.contenedor {
    width: 500px;
    margin: 0 auto;
}
h2 {
    text-align: center;
}
h5 {
    padding-left: 10px;
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
