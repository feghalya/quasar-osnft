<template>
  <q-page> 
    <div class="q-pa-md col">
      <h3 class='text-center' style='color: white;'>Our Team</h3>
      <div class='items-start q-gutter-md'>
        <q-card
          v-for="(member, index) in $store.state.nft_store.team"
          :key="`member=${index}`"
          class="my-card">
          <q-card-section>
            <div class='text-h6'>{{ member.name }}</div>
            <div class='text-subtitle'>{{ member.title }}</div>
            <href round type="a" href="member.linkedin_url" target='_blank' label="Linkedin"></href>
          </q-card-section>

          <q-card-section>
            <div>{{ member.desc }}</div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script>

import { useStore } from 'vuex'

export default {
  setup() {
    const $store = useStore()
    return{
      $store
    }
  }
}
</script>
<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 600px
</style>