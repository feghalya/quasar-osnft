<template>
  <q-page> 
    <div class="q-pa-md">
      <h5>Weekly Updates</h5>
      <q-list dense bordered padding separator class="rounded-borders">
        <q-item v-ripple v-for="update in $store.state.nft_store.weekly_update" :key="update.title">
          <q-item-section >
            <q-item-label >{{ update.title }}</q-item-label>
            <q-item-label caption>{{ update.date }}</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </div>
  </q-page>
</template>

<script lang='ts'>

import { useStore } from 'vuex'
import { defineComponent } from 'vue';
export default defineComponent({
  setup() {
    const $store = useStore()
  }
})

</script>