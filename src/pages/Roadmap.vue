<template>
<q-page>
  <div class='q-pa-md bigger-font white-font'>
      <h3 class='text-center white-font'>Roadmap</h3>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 1</p>
          <p>1 month</p>
        </div>
        <q-separator inset></q-separator>
          <ul>
            <li><p>
              Formally define the osNFT standard and its underlying legal component (Open-Source, CC-BY, etc.)
            </p></li>
            <li><p>
              Amass high-quality data and constructive feedback from high-profile PIs (Principal Investigators), from contacts at our
              workplace (academic high-tech research center).
            </p></li>
            <li><p>
              Generate primitive osNFTs from PhD student's work (beautiful microscopy photos, sexy graphs, etc.) as a proof of
              concept. Sciwalkart, one of the submitters of this proposal, would be more than happy to mint their artistic work as
              osNFTs.
            </p></li>
          </ul>
        <q-card-section>
        </q-card-section>
      </q-card>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 2</p>
          <p>4 month</p>
        </div>
        <q-separator inset></q-separator>
        <q-card-section>
          <ul>
            <li><p>
              Contact PIs from a curation of arxiv.org or PLOS papers for their potential enrolment in this project.
            </p></li>
            <li><p>
              Refine and finalize the osNFTs standard.
            </p></li>
            <li><p>
              Build a UI for the listing of the osNFTs on a decentralized hosting platform (Arweave permaweb).
            </p></li>
            <li><p>
              Start working on tutorials.
            </p></li>
          </ul>
        </q-card-section>
      </q-card>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 3</p>
          <p>6 month</p>
        </div>
        <q-separator inset></q-separator>

        <q-card-section>
          <ul>
            <li><p>
              Build an automated verification system that only allows copyright holders to submit their manuscripts (e.g., through
              the 'doi' standard).
            </p></li>
            <li><p>
              Start the minting process of manuscripts into osNFTs from interested scientists.
            </p></li>
            <li><p>
              Publicize the platform to generate public interest.
            </p></li>
          </ul>
        </q-card-section>
      </q-card>

      <q-card bordered class='roadmap-card'>
        <div class='roadmap-header'>
          <p class='subsection-title'>Phase 4</p>
          <p>12 month</p>
        </div>
        <q-separator inset></q-separator>
        <q-card-section>
          <ul>
            <li><p>
              System is gaining traction; potential scalability issues are being addressed.
            </p></li>
            <li><p>
              Marketplace is catching the public's eye; tutorials need to be updated.
            </p></li>
            <li><p>
              Adapt the whole experience based on user feedback.
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