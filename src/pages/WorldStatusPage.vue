<template>
  <q-page>
    <WorldStatuCardList />
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import WorldStatuCardList from '../components/WorldStatuCardList.vue';
export default defineComponent({
  name: 'WorldStatusPage',
  components: { WorldStatuCardList },
});
</script>
