<template>

  <q-layout view="lHh Lpr lFf" >

    <q-header elevatedclass="bg-black text-grey-8 z-top">
      <q-toolbar>

        <q-btn flat round dense icon="menu" @click="drawerLeft = !drawerLeft" />

        <q-avatar>
          <q-img src="icons/favicon-192x192.png" />
        </q-avatar>

        <q-toolbar-title class='text-weight-bold' v-if="titleName">
           Decentralized Open Science
        </q-toolbar-title>
        <q-toolbar-title class='text-weight-bold' v-else>
        </q-toolbar-title>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />

      </q-toolbar>
    </q-header>

    <q-drawer
      side="left"
      v-model="drawerLeft"
      :width="150"
      :breakpoint="700"
      behavior="desktop"
    >
      <q-scroll-area class="fit">

        <q-tabs
          vertical
          :breakpoint="500"
          class="text-white"
        >
          <q-route-tab name="Home" icon="home" label="Home" to="/" exact />
          <q-route-tab name="About" icon="description" label="In depth" to="/about" exact />
          <q-route-tab name="Roadmap" icon="list" label="Roadmap" to="/roadmap" exact />
          <q-route-tab name="Weekly Updates" icon="done_outline" label="Weekly Update" to="/weeklyUpdate" exact />
          <q-route-tab name="Team" icon="account_circle" label="About us" to="/team" exact />
         </q-tabs>

      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>


<script>

import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Twitter',
    caption: 'twitter.com/opensciencenft',
    icon: 'fab fa-twitter',
    link: 'https://twitter.com/opensciencenft'
  },
  {
    title: 'Facebook',
    caption: 'discord.com/invite/F8WxKFrc',
    icon: 'fab fa-discord',
    link: 'https://discord.com/invite/F8WxKFrc'
  },
  {
    title: 'Github',
    caption: 'github.com/intellart',
    icon: 'fab fa-github',
    link: 'https://github.com/intellart'
  }
];

import { defineComponent, ref } from 'vue'
import { useQuasar } from 'quasar'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },
  setup(){
    const $q = useQuasar()

    return {
      essentialLinks: linksList,
      drawerLeft: ref($q.screen.width > 700),
      titleName: ref($q.screen.width > 850)
    }
  }

})

</script>

<style lang="sass">
  .q-drawer
    background: #292e49

  .q-layout
    background: linear-gradient(to top, #536976, #292e49)
  
  .q-header
    background: #292e49
</style>
