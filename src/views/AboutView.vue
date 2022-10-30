<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button v-on:click="toHome">Перейти на домашнюю страницу</button>
  </div>
</template>
<script>
export default {
  name: "about",
  methods: {
    toHome() {
      return this.$router.push('/');
    },
  },
};
</script>