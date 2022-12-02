<template>
  <v-app>
    <NavBar></NavBar>
    <nuxt></nuxt>
  </v-app>
</template>

<script>
import NavBar from '../components/NavBar.vue';

export default {
  name: "DefaultLayout",
  data() {
    return {};
  },
  components: { NavBar }
}
</script>
<style lang="scss">
@import "~/assets/scss/main.scss";
</style>
