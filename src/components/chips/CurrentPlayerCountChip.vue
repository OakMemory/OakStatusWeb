<template>
  <q-chip color="purple" text-color="white" icon="people">
    {{ current }}
  </q-chip>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'CurrentPlayerCountChip',
  props: { current: { type: Number, default: 0 } },
});
</script>

<style></style>
