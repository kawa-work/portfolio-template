<template>
  <v-navigation-drawer app color="#C5CAE9">
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="text-h6">My Portfolio</v-list-item-title>
        <v-list-item-subtitle> Web Engineer Portfolio </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>

    <v-list dense nav>
      <v-list-item
        v-for="item in items"
        :key="item.title"
        :to="'#' + item.slag"
      >
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'Basic Info', icon: 'mdi-account-box', slag: 'basic' },
        { title: 'History', icon: 'mdi-school', slag: 'history' },
        { title: 'Skills', icon: 'mdi-hammer-wrench', slag: 'skills' },
        {
          title: 'Experience',
          icon: 'mdi-account-arrow-right',
          slag: 'experience',
        },
        { title: 'Research', icon: 'mdi-feature-search', slag: 'research' },
        { title: 'Work', icon: 'mdi-cube-outline', slag: 'work'},
      ],
    }
  },
}
</script>
