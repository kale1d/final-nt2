<template>
  <div id="app">
    <ContainerComponent />
  </div>
</template>

<script>
import ContainerComponent from './components/Container.vue'

export default {
  name: 'App',
  components: {
    ContainerComponent
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
