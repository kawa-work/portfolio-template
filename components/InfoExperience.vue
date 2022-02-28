<template>
  <v-card id="experience" class="my-12 pb-10" flat>
    <v-card-title>Experience</v-card-title>
    <v-card-text>
      <v-row class="justify-center">
        <v-col
          v-for="experience in experiences"
          :key="experience.company"
          cols="10"
        >
          <v-card>
            <v-card-title>
              {{ experience.company }}
            </v-card-title>
            <v-card-text>
              {{ experience.period }}
            </v-card-text>
            <v-card-text>
              {{ experience.description }}
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    experiences: [],
  }),
  async fetch() {
    this.experiences = await this.$content('experience').fetch()
  },
}
</script>
