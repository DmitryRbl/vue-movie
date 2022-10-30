<template>
  <div class="home">
    <h1>This is home page</h1>
    <button v-on:click="toAbout">Перейти на страницу about</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
  },
  methods: {
    toAbout() {
        return this.$router.push('/about');
    },
  },
}
</script>
