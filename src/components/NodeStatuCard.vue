<template>
  <div class="q-pa-md items-start status_card">
    <q-card class="bg-secondary text-white">
      <q-card-section>
        <div class="text-h6">Our Changing Planet</div>
      </q-card-section>

      <q-card-section>
        <div class="text-subtitle2">CPU Load: {{ cpu_load }}</div>
        <div class="text-subtitle2">Mem Load: {{ mem_load }}</div>
      </q-card-section>

      <q-separator dark />

      <q-card-actions align="right">
        <div v-if="is_online">
          <OnlineChip></OnlineChip>
        </div>
        <div v-else>
          <OfflineChip></OfflineChip>
        </div>
      </q-card-actions>
    </q-card>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import OnlineChip from './chips/OnlineChip.vue';
import OfflineChip from './chips/OfflineChip.vue';

export default defineComponent({
  name: 'NodeStatuCard',
  props: {
    node_name: {
      type: String,
      default: '',
    },
    cpu_load: {
      type: Number,
      default: 0.0,
    },
    mem_load: {
      type: Number,
      default: 0.0,
    },
    is_online: {
      type: Boolean,
      default: false,
    },
  },
  components: {
    OnlineChip,
    OfflineChip,
  },
});
</script>

<style lang="sass" scoped>
.status_card
  width: 400px
</style>
