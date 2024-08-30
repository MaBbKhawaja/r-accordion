<template>
  <div>
    <div @click="toggle()">
      <slot name="header"></slot>
    </div>
    <div class="box" v-if="open">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const open = ref(false)
const emit = defineEmits(['state'])

function toggle() {
      open.value = !open.value;
      if (open) {
        emit("state", "open");
      } else {
        emit("state", "close");
      }
    }
</script>

<style scoped>
</style>