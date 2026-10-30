<script setup>
import MediaPlaceholder from './MediaPlaceholder.vue'
import beidongshanTomb from '../assets/WhatSection/Research/Beidongshan tomb.webp'
import guishanTomb from '../assets/WhatSection/Research/Guishan tomb.webp'
import shizishanTomb from '../assets/WhatSection/Research/Shizishan tomb.webp'
import whatVideo from '../assets/WhatSection/what-video.mp4'
import demoVideo from '../assets/HowSection/Final Demo/Beidongshan_UnityDemo.mp4'
import demoCover from '../assets/HowSection/Final Demo/DemoVideoCover.png'
</script>

<template>
  <section id="what" class="what" aria-labelledby="what-heading">
    <div class="what__header grid-12">
      <div class="what__index">
        <span class="meta-label">Section</span>
        <p class="what__num">02</p>
      </div>
      <div class="what__heading-wrap">
        <hr class="hairline what__rule" />
        <h2 id="what-heading" class="what__heading">What Did I Do?</h2>
      </div>
    </div>

    <div class="what__lead grid-12">
      <MediaPlaceholder
        class="what__lead-video"
        type="video"
        :src="whatVideo"
        ratio="16 / 9"
        tone="a"
        fit="contain"
      />
    </div>

    <article class="what__entry">
      <hr class="hairline section-shell" />
      <div class="grid-12 what__row">
        <div class="what__text what__text--a">
          <h3 class="what__sub"># Historical Research</h3>
          <p class="what__body">
            For this project, I studied the history of the Han Dynasty, the
            architectural forms and structures of Han Dynasty tombs, Han beliefs
            surrounding life and death, and the general characteristics of the
            vassal kings’ tombs in Xuzhou. The Guishan, Shizishan, and Beidongshan
            tombs were constructed as underground worlds for the deceased Kings of
            Chu. Their chambers reproduced spaces associated with life above
            ground, while personal possessions and ceremonial objects were buried
            alongside the tomb owners.
          </p>
        </div>
        <div class="what__media what__media--a">
          <div class="what__gallery">
            <MediaPlaceholder
              fig="07"
              :src="beidongshanTomb"
              caption="Beidongshan tomb"
              ratio="16 / 10"
              fit="contain"
              tone="a"
              class="what__gal-main"
            />
            <MediaPlaceholder
              fig="08"
              :src="guishanTomb"
              caption="Guishan tomb"
              ratio="4 / 3"
              fit="contain"
              tone="c"
              class="what__gal-side"
            />
            <MediaPlaceholder
              fig="09"
              :src="shizishanTomb"
              caption="Shizishan tomb"
              ratio="4 / 5"
              fit="contain"
              tone="b"
              class="what__gal-side"
            />
          </div>
        </div>
      </div>
    </article>

    <article class="what__entry what__entry--last">
      <hr class="hairline section-shell" />
      <div class="grid-12 what__row what__row--b">
        <h3 class="what__heading what__demo-title">- Final Demo -</h3>
        <div class="what__media what__media--b">
          <MediaPlaceholder
            fig="10"
            type="video"
            :src="demoVideo"
            :poster="demoCover"
            caption="Experience recording"
            ratio="16 / 9"
            tone="c"
          />
        </div>
        <div class="what__text what__text--b">
          <h3 class="what__sub">
            # From Archaeological Evidence to Digital Reconstruction
          </h3>
          <p class="what__body">
            After developing a systematic understanding of these tombs, I selected
            the Beidongshan Han Tomb as the central subject of my project. I learned
            how to use 3D modelling to reconstruct historical architecture and used
            archaeological plans, excavation information, photographs, artefact
            records, and comparative references to recreate the tomb’s internal
            spaces and burial objects.
          </p>
          <p class="what__body what__body--follow">
            The final outcome is an interactive digital reconstruction of the
            Beidongshan Han Tomb. Rather than simply presenting the tomb as a
            static architectural model, the project allows users to explore it from
            a first-person perspective. Users can move through the reconstructed
            chambers, approach significant artefacts, and receive information about
            their historical purpose and cultural meaning. Lighting, sound, spatial
            organisation, and minimal interface elements are used to create an
            immersive and solemn atmosphere appropriate to the site.
          </p>
        </div>
      </div>
    </article>
  </section>
</template>

<style scoped>
.what {
  padding-block: clamp(3.5rem, 8vw, 6.5rem) clamp(4rem, 10vw, 8rem);
}

.what__header {
  align-items: end;
  margin-bottom: clamp(2rem, 4vw, 3rem);
}

.what__index {
  grid-column: 1 / span 2;
}

.what__num {
  margin-top: 0.35rem;
  font-size: clamp(1.5rem, 3vw, 2rem);
  letter-spacing: 0.08em;
  color: var(--bronze);
}

.what__heading-wrap {
  grid-column: 3 / span 10;
}

.what__rule {
  margin-bottom: 1.1rem;
}

.what__heading {
  font-size: clamp(1.25rem, 2.4vw, 1.75rem);
  font-weight: 400;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text);
}

.what__demo-title {
  grid-column: 1 / -1;
  margin-bottom: clamp(1.25rem, 3vw, 2rem);
  text-align: center;
}

.what__lead-video {
  grid-column: 3 / span 8;
}

.what__entry {
  padding-block: clamp(2.5rem, 5vw, 4rem);
}

.what__entry--last {
  padding-bottom: 0;
}

.what__row {
  padding-block: clamp(1.5rem, 3vw, 2.5rem) 0;
  align-items: start;
}

.what__sub {
  font-size: var(--lead);
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--text);
  margin-bottom: 1.1rem;
}

.what__body {
  font-size: var(--body);
  line-height: 1.8;
  color: var(--muted);
  max-width: 36rem;
}

.what__body--follow {
  margin-top: 1.1rem;
}

.what__text--a {
  grid-column: 1 / span 5;
  padding-top: 0.5rem;
}

.what__media--a {
  grid-column: 7 / span 6;
}

.what__media--b {
  grid-column: 3 / span 8;
}

.what__text--b {
  grid-column: 3 / span 8;
  margin-top: clamp(1.5rem, 3vw, 2.5rem);
}

.what__text--b .what__body {
  max-width: 40rem;
}

.what__gallery {
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: var(--gap);
  align-items: start;
}

.what__gal-main {
  grid-column: 1 / -1;
}

.what__gal-side:nth-child(2) {
  margin-top: 1.5rem;
}

@media (max-width: 960px) {
  .what__lead-video {
    grid-column: 1 / -1;
  }

  .what__index {
    grid-column: 1 / span 3;
  }

  .what__heading-wrap {
    grid-column: 4 / -1;
  }

  .what__text--a,
  .what__media--a,
  .what__media--b,
  .what__text--b {
    grid-column: 1 / -1;
  }

  .what__media--a {
    margin-top: 1.5rem;
  }
}

@media (max-width: 600px) {
  .what__gallery {
    grid-template-columns: 1fr;
  }

  .what__gal-side:nth-child(2) {
    margin-top: 0;
  }
}
</style>
