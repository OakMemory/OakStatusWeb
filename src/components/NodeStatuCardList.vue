<template>
  <div class="fit row wrap justify-start items-start content-start">
    <NodeStatuCard></NodeStatuCard>
    <NodeStatuCard></NodeStatuCard>
    <NodeStatuCard></NodeStatuCard>
    <NodeStatuCard></NodeStatuCard> <NodeStatuCard></NodeStatuCard>
    <NodeStatuCard></NodeStatuCard>
    <NodeStatuCard></NodeStatuCard>
    <NodeStatuCard></NodeStatuCard>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import NodeStatuCard from './NodeStatuCard.vue';

export default defineComponent({
  components: { NodeStatuCard },
  name: 'NodeStatuCardList',
  props: {},
  setup() {
    return {};
  },
});
</script>
