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

        <q-toolbar-title>
          Open Science NFT
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />

        <q-item-label header>
          Navigation
        </q-item-label>

        <q-item
          to="/"
          exact
          clickable
          v-ripple>
          
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>

          <q-item-section>
            Home
          </q-item-section>
        </q-item>

        <q-item
          to="/about"
          exact
          clickable
          v-ripple>
          <q-item-section avatar>
            <q-icon name="description" />
          </q-item-section>

          <q-item-section>
            About
          </q-item-section>
        </q-item>

        <q-item
          to="/team"
          exact
          clickable
          v-ripple>

          <q-item-section avatar>
            <q-icon name="people" />
          </q-item-section>

          <q-item-section>
            Team
          </q-item-section>
        </q-item>

        <q-item
          to="/weeklyUpdate"
          exact
          clickable
          v-ripple>
          
          <q-item-section avatar>
            <q-icon name="event_note" />
          </q-item-section>

          <q-item-section>
            Weekly Update
          </q-item-section>
        </q-item>

        <q-item
          to="/roadmap"
          exact
          clickable
          v-ripple>
          
          <q-item-section avatar>
            <q-icon name="insights" />
          </q-item-section>

          <q-item-section>
            Roadmap
          </q-item-section>
        </q-item>

      </q-list>
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
    title: 'Github',
    caption: 'github.com/quasar-osnft',
    icon: 'code',
    link: 'https://github.com/louisgendron26/quasar-osnft'
  },
  {
    title: 'Twitter',
    caption: 'Coming soon',
    icon: 'rss_feed',
    link: 'https://twitter.com'
  },
  {
    title: 'Facebook',
    caption: 'Coming soon',
    icon: 'public',
    link: 'https://facebook.com'
  },
];

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
