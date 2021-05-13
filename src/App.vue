<template>
  <div id="app">
    <Form_List />
    
  </div>
</template>

<script>
import Form_List from './components/Form_List'
export default {
  name: 'App',
  components: {
    Form_List,
  }
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
  width: 1170px;
  margin-left: auto;
  margin-right: auto;
}
</style>
