<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Oak Memory Server Status </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Status </q-item-label>

        <SideBarLink
          v-for="link in statuLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <SideBarLink
          v-for="link in usefulLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <transition
        appear
        enter-active-class="animated fadeIn"
        leave-active-class="animated fadeOut"
      >
        <router-view />
      </transition>
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import SideBarLink from 'src/components/SideBarLink.vue';

const usefulLinks = [
  {
    title: 'Skin Server',
    caption: 'Oak Memory Skin',
    icon: 'account_circle',
    link: 'https://skin.krysztal.dev',
  },
];

const statuLinks = [
  {
    title: 'Index Page',
    caption: 'The home',
    icon: 'layers',
    link: '/#/',
  },
  {
    title: 'Node Status',
    caption: 'View all node status',
    icon: 'dns',
    link: '/#/node_status',
  },
  {
    title: 'Player Status',
    caption: 'View all player status',
    icon: 'groups',
    link: '/#/player_status',
  },
  {
    title: 'World Status',
    caption: 'View all world status',
    icon: 'public',
    link: '/#/world_status',
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    SideBarLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      usefulLinks: usefulLinks,
      statuLinks: statuLinks,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
