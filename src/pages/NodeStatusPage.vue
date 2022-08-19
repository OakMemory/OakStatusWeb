<template>
  <q-page class="row items-center justify-evenly">
    <NodeStatuCardList></NodeStatuCardList>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import NodeStatuCardList from 'components/NodeStatuCardList.vue';
export default defineComponent({
  name: 'NodeStatusPage',
  components: { NodeStatuCardList },
});
</script>
