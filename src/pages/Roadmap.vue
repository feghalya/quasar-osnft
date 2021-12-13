<template>
<q-page>
  <div class='q-pa-md bigger-font white-font'>
      <h3 class='text-center white-font'>Timeline</h3>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 1</p>
          <p>Q1 2022</p>
        </div>
        <q-separator inset></q-separator>
        <q-card-section>
          <ul>
            <li><p>
              Formally define the osNFT standard and its underlying legal component (Open-Source, CC-BY, etc.)
            </p></li>
            <li><p>
              Finalize cross-bridge NFT minting (data+metadata) from Arweave to Cardano.
            </p></li>
          </ul>
        </q-card-section>
      </q-card>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 2</p>
          <p>Q2 2022</p>
        </div>
        <q-separator inset></q-separator>
        <q-card-section>
          <ul>
            <li><p>
              Complete osNFT framework #1: C. elegans developmental stages.
            </p></li>
            <li><p>
              Endorsement-based staking beta-functionality.
            </p></li>
          </ul>
        </q-card-section>
      </q-card>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 3</p>
          <p>Q3 2022</p>
        </div>
        <q-separator inset></q-separator>

        <q-card-section>
          <ul>
            <li><p>
              Complete osNFT framework #2: Modular biological cells.
            </p></li>
            <li><p>
              Public launch of the marketplace.
            </p></li>
          </ul>
        </q-card-section>
      </q-card>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 4</p>
          <p>Q4 2022</p>
        </div>
        <q-separator inset></q-separator>
        <q-card-section>
          <ul>
            <li><p>
              Build an automated verification system that only allows copyright holders to submit their manuscripts (e.g., through
              the 'doi' standard).
            </p></li>
            <li><p>
              Collecting feedback and iterating with enhancements.
            </p></li>
          </ul>
        </q-card-section>
      </q-card>
  </div>
</q-page>
</template>

<script>
  export default {
    
  }
</script>

<style lang="sass">
.q-card
    background: linear-gradient(to bottom, #536976, #292e49)
</style>
