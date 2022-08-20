<template>
  <q-page>
    <PlayerStatuCardList />
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PlayerStatuCardList from '../components/PlayerStatuCardList.vue';
export default defineComponent({
  name: 'PlayerStatusPage',
  components: { PlayerStatuCardList },
});
</script>
