<template>
  <q-page>
    <div class="q-pa-md col white-font">
      <h3 class='text-center'>Team</h3>

      <div class='row bigger-font'>

        <div class='col-sm-8 offset-sm-2 q-gutter-md'>
          <q-card
            v-for="(member, index) in store.state.nft_store.team"
            :key="`member=${index}`"
            class="my-card">

            <q-card-section>

              <q-item>

                <q-item-section avatar>
                  <q-avatar size="172px">
                    <q-img :src="'people/'+member.photo" />
                  </q-avatar>
                </q-item-section>

                <q-item-section
                  v-if='memberName'
                  class='white-font'
                  side>
                  <p style="margin-bottom:0px; font-size: 150%"> {{ member.name }} </p>
                  <p style="margin-bottom:0px; font-size: 100%"> {{ member.title }} </p>
                </q-item-section>

                <q-item-section></q-item-section>

                <q-item-section side class='white-font'>
                  <q-icon
                    v-if="member.linkedin_url"
                    class='linkedin-icon'
                    size='md'
                    name='fab fa-linkedin'
                    clickable
                    @click="openHref(member.linkedin_url)">
                  </q-icon>

                   <q-icon
                    v-if="member.website_url"
                    style="margin-top:20px;"
                    class='globe-icon'
                    size='md'
                    name='fas fa-globe'
                    clickable
                    @click="openHref(member.website_url)">
                  </q-icon>

                   <q-icon
                    v-if="member.instagram_url"
                    style="margin-top:20px;"
                    class='instagram-icon'
                    size='md'
                    name='fab fa-instagram'
                    clickable
                    @click="openHref(member.instagram_url)">
                  </q-icon>

                </q-item-section>

              </q-item>

            </q-card-section>

            <q-card-section v-if='!memberName' class='white-font'>
              <p style="margin-bottom:0px; font-size: 150%"> {{ member.name }} </p>
              <p style="margin-bottom:0px; font-size: 100%"> {{ member.title }} </p>
            </q-card-section>

            <q-separator inset></q-separator>

            <q-card-section>
              {{ member.desc }}
            </q-card-section>

          </q-card>
        </div>

      </div> <!-- Row -->
    </div>

   <div class="q-pa-md col white-font">
      <h3 class='text-center'>Advisors</h3>

      <div class='row bigger-font'>

        <div class='col-sm-8 offset-sm-2 q-gutter-md'>
          <q-card
            v-for="(member, index) in store.state.nft_store.advisors"
            :key="`member=${index}`"
            class="my-card">

            <q-card-section>

              <q-item>

                <q-item-section avatar>
                  <q-avatar size="172px">
                    <q-img :src="'people/'+member.photo" />
                  </q-avatar>
                </q-item-section>

                <q-item-section
                  v-if='memberName'
                  class='white-font'
                  side>
                  <p style="margin-bottom:0px; font-size: 150%"> {{ member.name }} </p>
                  <p style="margin-bottom:0px; font-size: 100%"> {{ member.title }} </p>
                </q-item-section>

                <q-item-section></q-item-section>

                <q-item-section side class='white-font'>
                  <q-icon
                    v-if="member.linkedin_url"
                    class='linkedin-icon'
                    size='md'
                    name='fab fa-linkedin'
                    clickable
                    @click="openHref(member.linkedin_url)">
                  </q-icon>

                   <q-icon
                    v-if="member.website_url"
                    style="margin-top:20px;"
                    class='globe-icon'
                    size='md'
                    name='fas fa-globe'
                    clickable
                    @click="openHref(member.website_url)">
                  </q-icon>

                   <q-icon
                    v-if="member.instagram_url"
                    style="margin-top:20px;"
                    class='instagram-icon'
                    size='md'
                    name='fab fa-instagram'
                    clickable
                    @click="openHref(member.instagram_url)">
                  </q-icon>

                </q-item-section>

              </q-item>

            </q-card-section>

            <q-card-section v-if='!memberName' class='white-font'>
              <p style="margin-bottom:0px; font-size: 150%"> {{ member.name }} </p>
              <p style="margin-bottom:0px; font-size: 100%"> {{ member.title }} </p>
            </q-card-section>

            <q-separator inset></q-separator>

            <q-card-section>
              {{ member.desc }}
            </q-card-section>

          </q-card>
        </div>

      </div> <!-- Row -->
    </div>

  </q-page>
</template>

<script>

import { ref } from 'vue'
import { useStore } from 'vuex'
import { useQuasar } from 'quasar'

export default {
  methods: {
    openHref(url){
      window.open(String(url), '_blank');
    }
  },
  setup() {
    const store = useStore()
    const q = useQuasar()
    return{
      store,
      memberName: ref(q.screen.width > 850)
    }
  }
}

</script>

<style lang="sass">
  .q-card
    background: linear-gradient(to bottom, #536976, #292e49)
</style>
