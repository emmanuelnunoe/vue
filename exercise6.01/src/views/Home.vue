<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <input type="button" value="Mesaages" @click="navegar()" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'Home',
  methods: {
    navegar: function() {
      this.$router.push('/messages');
    },
  },
  components: {
    HelloWorld,
  },
};
</script>
