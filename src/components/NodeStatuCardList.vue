<template>
  <div class="fit row justify-center">
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
    <NodeStatuCard />
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
