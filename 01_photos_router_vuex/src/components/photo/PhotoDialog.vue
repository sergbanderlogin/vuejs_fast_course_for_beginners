<template>
  <v-dialog
      v-model="$store.getters.getDialogVisible"
      max-width="600"
      @click:outside="$store.commit('hideDialog')"
  >
    <v-card>
      <v-card-title>{{ full_title }}</v-card-title>
      <v-card-text>
        <v-img
            :src="$store.getters.getCurrentPhoto.url"
        />
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  name: "PhotoDialog.vue",
  computed: {
    full_title() {
      return `Назва фотографії - ${this.$store.getters.getCurrentPhoto.title}`
    }
  },
}
</script>

<style scoped>

</style>