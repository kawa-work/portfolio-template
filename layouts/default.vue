<template>
  <v-app>
    <TheSidebar></TheSidebar>
    <v-main class="secondary">
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
