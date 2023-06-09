<template>
  <PTable />
</template>

<script>
import PTable from './components/PTable.vue'

export default {
  name: 'App',
  components: {
    PTable
  }
}
</script>

<style>
#app {
  font-family: Segoe UI, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f8f8f2;
  background-color: #282a36;
}

html {
  background-color: #282a36;
}
</style>
