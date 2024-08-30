<script setup lang="ts">
import Accordion from './components/Accordion.vue'

</script>

<template>
  <Accordion>
    <template v-slot:header>
    <!-- content for the header slot -->
     hello
  </template>
  <template v-slot:content>
    <!-- content for the header slot -->
     this is anees
  </template>
    </Accordion>
</template>

<style scoped>
</style>
