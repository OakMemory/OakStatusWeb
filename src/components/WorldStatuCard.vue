<template>
  <div class="player_statu_card">
    <q-card>
      <q-card-section horizontal>
        <q-card-section class="q-pt-xs">
          <div class="text-h5 q-mt-sm q-mb-xs col-8">{{ name }}</div>
        </q-card-section>
      </q-card-section>

      <!-- Chips -->
      <q-card-actions align="right">
        <CurrentPlayerCountChip :current="current" />
        <HeavyStatuChip />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeavyStatuChip from './chips/HeavyStatuChip.vue';
import CurrentPlayerCountChip from './chips/CurrentPlayerCountChip.vue';

export default defineComponent({
  name: 'WorldStatuCard',
  props: {
    name: { type: String, default: 'unknown' },
    current: { type: Number, default: 0 },
  },
  components: { HeavyStatuChip, CurrentPlayerCountChip },
  setup() {
    return {};
  },
});
</script>

<style lang="sass" scoped>
.player_statu_card
  width: 80%
  margin-top:16px
</style>
