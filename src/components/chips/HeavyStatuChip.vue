<template>
  <div v-if="is_heavy">
    <q-chip color="green" text-color="white" icon="check" label="OK" />
  </div>

  <div v-else>
    <q-chip color="red" text-color="white" icon="close" label="HEAVY" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HeavyStatuChip',
  props: { is_heavy: { type: Boolean, default: true } },
});
</script>

<style></style>
