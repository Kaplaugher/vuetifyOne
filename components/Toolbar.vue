<template>
  <v-toolbar dark color="blue">
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title class="white--text">
      <nuxt-link class="title" to='/'>Itunes Search</nuxt-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn to='/' icon>
      <v-icon>refresh</v-icon>
    </v-btn>
  </v-toolbar>
</template>

<script>
export default {};
</script>

<style scoped>

.title {
  text-decoration: none !important;
}

.title:visited {
  color: white;
}

</style>
