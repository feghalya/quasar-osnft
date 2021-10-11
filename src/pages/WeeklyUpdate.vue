<template>
  <q-page> 
    <div class="q-pa-md white-font">
      <h3 class='text-center'>Weekly Updates</h3>
      <div class='row bigger-font'>
        <div class='col-sm-8 offset-sm-2 q-gutter-md'>
        <q-list dense bordered padding separator
          class='rounded-borders update-list'
          style='border-width: 5px'>
          <q-item
            v-ripple v-for="(update, index) in $store.state.nft_store.weekly_update"
            :key="`update-${index}`">
            <q-item-section side>
              <q-item-label class="white-font">{{ update.date }}</q-item-label>
            </q-item-section>

            <q-item-section>
              <q-item-label class="white-font">{{ update.title }}</q-item-label>
            </q-item-section>
          </q-item>

        </q-list>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>

import { useStore } from 'vuex'
import { defineComponent } from 'vue';

export default {
  setup() {
    const $store = useStore()
    return{
      $store
    }
  }
}
</script>

<style lang="sass">
.update-list
    background: linear-gradient(to bottom, #536976, #292e49)
</style>