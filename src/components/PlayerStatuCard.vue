<template>
  <div class="player_statu_card">
    <q-card>
      <q-card-section horizontal>
        <q-card-section class="q-pt-xs">
          <div class="text-h5 q-mt-sm q-mb-xs">{{ name }}</div>
        </q-card-section>

        <q-card-section class="col-5 flex"> </q-card-section>
      </q-card-section>

      <!-- Chips -->
      <q-card-actions align="right">
        <PermissionChip :perm="perm" />
        <OnlineStatuChip :is_online="is_online" />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PermissionChip from './chips/PermissionChip.vue';
import OnlineStatuChip from './chips/OnlineStatuChip.vue';

export default defineComponent({
  name: 'PlayerStatuCard',
  props: {
    name: { type: String, default: 'unknown' },
    max_heal: { type: Number, default: 20 },
    heal: { type: Number, default: 20 },
    perm: { type: String, default: 'Player' },
    is_online: { type: Boolean, default: false },
  },
  components: { PermissionChip, OnlineStatuChip },
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
