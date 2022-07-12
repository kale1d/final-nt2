<template>
  <div>
    <div class="input-container">
      <div>
        <label for="color">Color: </label>
        <input name="color" type="text" v-model="color" />
      </div>
      <div>
        <label for="fondo">Fondo: </label>
        <input name="fondo" type="text" v-model="fondo" />
      </div>
      <div>
        <label for="size">Size: </label>
        <input name="size" type="text" v-model="size" />
      </div>
    </div>
    <div class="text-container">
      <div>
        <label for="texto">Texto: </label>
        <input name="texto" type="text" v-model="texto"
          :style="{ backgroundColor: fondo, color: color, fontSize: size }" />
      </div>
    </div>
    <div v-if="texto.length">
      <p>Cantidad de palabras: {{ cantPalabras }}</p>
    </div>
    <div>
      <h1>Respuestas</h1>
      <table>
        <thead>
          <tr>
            <th>Numero de pregunta</th>
            <th>Numero de respuesta</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th>1</th>
            <th>b</th>
          </tr>
          <tr>
            <th>2</th>
            <th>c</th>
          </tr>
          <tr>
            <th>3</th>
            <th>b</th>
          </tr>
          <tr>
            <th>4</th>
            <th>d</th>
          </tr>
          <tr>
            <th>5</th>
            <th>d</th>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContainerComponent',
  data() {
    return {
      color: '',
      fondo: '',
      size: 20,
      texto: '',
    }
  },
  computed: {
    cantPalabras() {

      const arr = this.texto.split(' ');
      return arr.filter(word => word !== '').length;
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="css">
.input-container {
  width: 60vw;
  display: flex;
  justify-content: space-between;
}

.text-container {
  margin-top: 5vh;
}

table,
th,
td {
  border: 1px solid;
}
</style>
