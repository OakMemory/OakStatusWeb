<template>
  <div v-if="is_online">
    <q-chip color="green" text-color="white" icon="check" label="Online" />
  </div>

  <div v-else>
    <q-chip color="red" text-color="white" icon="close" label="Offline" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'OnlineStatuChip',
  props: { is_online: { type: Boolean, default: false } },
});
</script>

<style></style>
