<template>
  <div id="app">
    <MyPerson name="清华大学" address="北京" :num="22"/>
    <hr/>
    <MyPerson :school="school"/>
  </div>
</template>

<script>
import MyPerson from './components/MyPerson.vue'

export default {
  name: 'App',
  components: {
    MyPerson
  },
  data() {
    return {
      school: {
        name: '复旦大学',
        address: '上海',
      }
    }
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
}
</style>
