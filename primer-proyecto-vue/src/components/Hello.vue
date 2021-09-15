<template>
  <div>
    <h1>Hello {{ who }}</h1>
    <h2>{{ saludo }}</h2>
    <h3>and Hello {{ otherName }}</h3>
  </div>
</template>

<script>
export default {
  props: ['who', 'saludo', 'otherName'],
};
</script>

<style></style>
