<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title class='text-weight-bold'>
          osNFT Standard
        </q-toolbar-title>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
        </q-toolbar>
        <q-tabs>
          <q-list class='row justify-center full-height full-width text-center white-font' style='font-size: 150%'>
            
            <q-item to="/" exact flat round dense> 
              <q-item-section >
                Home
              </q-item-section>
            </q-item>

            <q-item to="/about" exact> 
              <q-item-section>
                About
              </q-item-section>
            </q-item>

            <q-item to="/roadmap" exact> 
              <q-item-section>
                Roadmap
              </q-item-section>
            </q-item>

            <q-item to="/weeklyUpdate" exact> 
              <q-item-section>
                Weekly Update
              </q-item-section>
            </q-item>

            <q-item to="/team" exact> 
              <q-item-section>
                Team
              </q-item-section>
            </q-item>

          </q-list>
        </q-tabs>
    </q-header>

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
    icon: 'fab fa-github',
    link: 'https://github.com/louisgendron26/quasar-osnft'
  },
  {
    title: 'Twitter',
    caption: 'Coming soon',
    icon: 'fab fa-twitter',
    link: 'https://twitter.com'
  },
  {
    title: 'Facebook',
    caption: 'Coming soon',
    icon: 'fab fa-facebook',
    link: 'https://facebook.com'
  },
];

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
   EssentialLink,
  },
  setup(){
    return {
      essentialLinks: linksList,
    }
  }

})
</script>

<style lang="sass">
  .q-layout
    background: linear-gradient(to top, #536976, #292e49)
  
  
  .q-header
    background: #292e49
</style>
