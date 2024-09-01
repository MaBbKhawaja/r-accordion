<script setup lang="ts">
import Accordion from './components/Accordion.vue'

</script>

<template>
  <Accordion>
    <template v-slot:header>
      <!-- content for the header slot -->
      hello
    </template>
    <div>
      this is anees baig
    </div>
  </Accordion>
  <Accordion header="I am a header">
    <div>
      this is anees baig
    </div>
  </Accordion>
</template>

<style scoped>
</style>
