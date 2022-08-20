<template>
  <div v-if="perm == 'Player'">
    <q-chip color="green" text-color="white" icon="account_circle">{{
      perm
    }}</q-chip>
  </div>
  <div v-else-if="perm == 'Op'">
    <q-chip color="red" text-color="white" icon="admin_panel_settings">{{
      perm
    }}</q-chip>
  </div>
  <div v-else>
    <q-chip color="blue" text-color="white" icon="people_alt">{{
      perm
    }}</q-chip>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PermissionChip',
  props: { perm: { type: String, default: 'Player' } },
});
</script>

<style></style>
