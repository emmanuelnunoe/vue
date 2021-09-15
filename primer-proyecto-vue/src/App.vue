<template>
  <div id="app">
    <!-- <input type="text" v-model="name" />
    <Hello :otherName="this.name" who="Emmanuel" saludo="Buenos dias" /> -->
    <h1>Info equipo by ID</h1>
    Team ID:<input type="text" v-model="teamId" />
    <InfoEquipo :id="this.teamId" />
  </div>
</template>

<script>
import InfoEquipo from './components/InfoEquipo.vue';
export default {
  name: 'App',
  data() {
    return {
      name: '',
      teamId: '',
    };
  },
  components: {
    InfoEquipo,
  },
};
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
