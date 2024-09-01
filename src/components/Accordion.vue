<template>
  <div>
    <div @click="toggle()">
      <slot name="header">
        {{ props.header ?? props.header }}
      </slot>
    </div>
    <div class="box" v-if="open">
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const open = ref(false)
const emit = defineEmits(['state'])
const props = defineProps(['header'])

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