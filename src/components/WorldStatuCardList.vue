<template>
  <div class="fit row wrap justify-center items-start content-start">
    <WorldStatuCard />
    <WorldStatuCard />
    <WorldStatuCard />
    <WorldStatuCard />
    <WorldStatuCard />
    <WorldStatuCard />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import WorldStatuCard from './WorldStatuCard.vue';

export default defineComponent({
  name: 'PlayerStatuCardList',
  components: { WorldStatuCard },
  props: {},
  setup() {
    return {};
  },
});
</script>
