<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h3>{{ user }}</h3>
  </div>
</template>

<script>
export default {
  props: ['user'],
};
</script>
