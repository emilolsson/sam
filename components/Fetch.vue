<template>
  <div id="Fetch" class="Fetch col col-100">

    <div v-html="document.data">

    </div>

  </div>
</template>

<script>
export default {
  data: () => ({
    document: { data: { intro_text: null } },
  }),
  async fetch() {
      try {
        this.document = await this.$prismic.client.getSingle('homepage')
      } catch {
        this.$nuxt.error({ statusCode: 404, message: "Data not found" });
      }
  },
}
</script>

<style lang="scss">
.Fetch {
  background: blue;
}
</style>
