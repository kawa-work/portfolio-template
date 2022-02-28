<template>
  <v-app>
    <TheSidebar></TheSidebar>
    <v-main class="indigo lighten-5">
      <nuxt />
    </v-main>
    <TheFooter></TheFooter>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>
