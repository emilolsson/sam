<template>
  <div class="container">
    <Fetch />
  </div>
</template>

<script>
import Fetch from '~/components/Fetch.vue'

export default {
  components: {
    Fetch,
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
