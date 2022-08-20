<template>
  <div class="fit row wrap justify-center items-start content-start">
    <PlayerStatuCard />
    <PlayerStatuCard />
    <PlayerStatuCard />
    <PlayerStatuCard />
    <PlayerStatuCard />
    <PlayerStatuCard />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PlayerStatuCard from './PlayerStatuCard.vue';

export default defineComponent({
  name: 'PlayerStatuCardList',
  components: { PlayerStatuCard },
  props: {},
  setup() {
    return {};
  },
});
</script>
