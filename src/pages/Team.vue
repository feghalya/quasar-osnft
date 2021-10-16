<template>
  <q-page> 
    <div class="q-pa-md col white-font">
      <h3 class='text-center'>Who we are</h3>
      <div class='row bigger-font'>

        <div class='col-sm-8 offset-sm-2 q-gutter-md'>
          <q-card
            v-for="(member, index) in store.state.nft_store.team"
            :key="`member=${index}`"
            class="my-card">

            <q-card-section>

              <q-item >

                <q-item-section
                  class='white-font'
                  style='font-size: 150%'
                  side>
                  {{ member.name }}
                </q-item-section>

                <q-item-section class='white-font'>
                  <p style="margin-left: 20px; margin-bottom:0px"> {{ member.title }} </p>
                </q-item-section>

                <q-item-section side class='white-font' v-if="member.website_url">
                   <q-icon
                    class='globe-icon'
                    size='md'
                    name='fas fa-globe'
                    clickable
                    @click="openHref(member.website_url)">
                  </q-icon>
                </q-item-section>

                <q-item-section side class='white-font' v-if="member.instagram_url">
                   <q-icon
                    class='instagram-icon'
                    size='md'
                    name='fab fa-instagram'
                    clickable
                    @click="openHref(member.instagram_url)">
                  </q-icon>
                </q-item-section>

                <q-item-section side class='white-font' v-if="member.linkedin_url">
                  <q-icon
                    class='linkedin-icon'
                    size='md'
                    name='fab fa-linkedin'
                    clickable
                    @click="openHref(member.linkedin_url)">
                  </q-icon>
                </q-item-section>

              </q-item>

            </q-card-section>

            <q-separator inset></q-separator>

            <q-card-section>
              <div>{{ member.desc }}</div>
            </q-card-section>

          </q-card>
        </div>

      </div> <!-- Row -->
    </div>

   <div class="q-pa-md col white-font">
      <h3 class='text-center'>Our Advisors and Sponsors</h3>
      <div class='row bigger-font'>

        <div class='col-sm-8 offset-sm-2 q-gutter-md'>
          <q-card
            v-for="(member, index) in store.state.nft_store.advisors"
            :key="`member=${index}`"
            class="my-card">

            <q-card-section>

              <q-item >

                <q-item-section
                  class='white-font'
                  style='font-size: 150%'
                  side>
                  {{ member.name }}
                </q-item-section>

                <q-item-section class='white-font'>
                  <p style="margin-left: 20px; margin-bottom:0px"> {{ member.title }} </p>
                </q-item-section>

                <q-item-section side class='white-font' v-if="member.website_url">
                   <q-icon
                    class='globe-icon'
                    size='md'
                    name='fas fa-globe'
                    clickable
                    @click="openHref(member.website_url)">
                  </q-icon>
                </q-item-section>

                <q-item-section side class='white-font' v-if="member.instagram_url">
                   <q-icon
                    class='instagram-icon'
                    size='md'
                    name='fab fa-instagram'
                    clickable
                    @click="openHref(member.instagram_url)">
                  </q-icon>
                </q-item-section>

                <q-item-section side class='white-font' v-if="member.linkedin_url">
                  <q-icon
                    class='linkedin-icon'
                    size='md'
                    name='fab fa-linkedin'
                    clickable
                    @click="openHref(member.linkedin_url)">
                  </q-icon>
                </q-item-section>

              </q-item>

            </q-card-section>

            <q-separator inset></q-separator>

            <q-card-section>
              <div>{{ member.desc }}</div>
            </q-card-section>

          </q-card>
        </div>

      </div> <!-- Row -->
    </div>

  </q-page>
</template>

<script>

import { useStore } from 'vuex'

export default {
  methods:{
    openHref(url){
      window.open(String(url), '_blank');
    }
  },
  setup() {
    const store = useStore()
    return{
      store
    }
  }
}
</script>
<style lang="sass">
  .q-card
    background: linear-gradient(to bottom, #536976, #292e49)
</style>