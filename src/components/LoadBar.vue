<template>
  <q-linear-progress
    size="50px"
    :value="progress"
    color="accent"
    class="q-mt-sm"
  >
    <div class="absolute-full flex flex-center">
      <q-badge color="white" text-color="accent" :label="progressLable" />
    </div>
  </q-linear-progress>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoadBar',
  props: {
    max_heavy: { type: Number, default: 20 },
    current_heavy: { type: Number, default: 0 },
  },

  setup() {
    return {};
  },
  computed: {
    progress() {
      return this.current_heavy / this.max_heavy;
    },
    progressLable() {
      return (this.current_heavy / this.max_heavy) * 100 + '%';
    },
  },
});
</script>
