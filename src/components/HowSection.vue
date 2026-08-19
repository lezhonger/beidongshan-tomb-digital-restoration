<script setup>
import MediaPlaceholder from './MediaPlaceholder.vue'

import tombPlan from '../assets/HowSection/Research/Plan of the Tomb of the King of Chu at Beidongshan.webp'
import tombPerspective from '../assets/HowSection/Research/Perspective view of the Tomb of the King of Chu at Beidongshan.webp'
import site1 from '../assets/HowSection/Research/Site-photos1.webp'
import site2 from '../assets/HowSection/Research/Site-photos2.webp'
import site3 from '../assets/HowSection/Research/Site-photos3.webp'
import site4 from '../assets/HowSection/Research/Site-photos4.webp'
import site5 from '../assets/HowSection/Research/Site-photos5.webp'
import site6 from '../assets/HowSection/Research/Site-photos6.webp'
import layoutRef from '../assets/HowSection/Building/TombLayout-Reference.webp'
import layoutWhite from '../assets/HowSection/Building/TombLayout-WhiteModel.webp'
import layoutTextured from '../assets/HowSection/Building/TombLayout-TexturedModel.webp'
import coffinRef from '../assets/HowSection/Building/Treasure-Coffin-Ref.webp'
import coffinWhite from '../assets/HowSection/Building/Treasure-Coffin-WhiteModel.webp'
import coffinTextured from '../assets/HowSection/Building/Treasure-Coffin-Textured.webp'
import dancerRef1 from '../assets/HowSection/Building/Treasure-DancingFiguries1-Ref.webp'
import dancerRef2 from '../assets/HowSection/Building/Treasure-DancingFiguries2-Ref.webp'
import dancerRef3 from '../assets/HowSection/Building/Treasure-DancingFiguries3-Ref.webp'
import dancerWhite from '../assets/HowSection/Building/Treasure-DancingFiguries-WhiteModel.webp'
import dancerTextured from '../assets/HowSection/Building/Treasure-DancingFiguries-Textured.webp'
import jadeSuitRef from '../assets/HowSection/Building/Treasure-Sewn-Ref.webp'

const steps = [
  {
    id: '01',
    title: '#1 Research & Reference',
    tag: '01 / Research',
    reverse: false,
    groups: [
      {
        id: 'drawings',
        label: 'Archaeological drawings',
        cols: 2,
        figs: [
          {
            fig: '12',
            src: tombPlan,
            caption: 'Plan of the tomb',
            tone: 'a',
            ratio: '3 / 4',
            fit: 'contain',
          },
          {
            fig: '13',
            src: tombPerspective,
            caption: 'Perspective view of the tomb',
            tone: 'b',
            ratio: '3 / 4',
            fit: 'contain',
          },
        ],
      },
      {
        id: 'site',
        label: 'Site photographs — Beidongshan',
        cols: 3,
        figs: [
          { fig: '14', src: site1, tone: 'c', ratio: '1 / 1' },
          { fig: '15', src: site2, tone: 'a', ratio: '1 / 1' },
          { fig: '16', src: site3, tone: 'b', ratio: '1 / 1' },
          { fig: '17', src: site4, tone: 'c', ratio: '1 / 1' },
          { fig: '18', src: site5, tone: 'a', ratio: '1 / 1' },
          { fig: '19', src: site6, tone: 'b', ratio: '1 / 1' },
        ],
      },
    ],
  },
  {
    id: '02',
    title: '#2 Building the Space',
    tag: '02 / Space',
    reverse: true,
    groups: [
      {
        id: 'layout',
        label: 'Tomb layout',
        cols: 3,
        figs: [
          {
            fig: '20',
            src: layoutRef,
            caption: 'Reference',
            tone: 'a',
            ratio: '16 / 10',
            fit: 'contain',
          },
          { fig: '21', src: layoutWhite, caption: 'White model', tone: 'b', ratio: '16 / 10' },
          { fig: '22', src: layoutTextured, caption: 'Textured model', tone: 'c', ratio: '16 / 10' },
        ],
      },
      {
        id: 'coffin',
        label: 'Coffin',
        cols: 3,
        figs: [
          {
            fig: '23',
            src: coffinRef,
            caption: 'Reference',
            tone: 'a',
            ratio: '16 / 10',
            fit: 'contain',
          },
          { fig: '24', src: coffinWhite, caption: 'White model', tone: 'b', ratio: '16 / 10' },
          { fig: '25', src: coffinTextured, caption: 'Textured model', tone: 'c', ratio: '16 / 10' },
        ],
      },
      {
        id: 'dancers-ref',
        label: 'Dancing figurines — references',
        cols: 3,
        figs: [
          { fig: '26', src: dancerRef1, tone: 'a', ratio: '4 / 5', fit: 'contain' },
          { fig: '27', src: dancerRef2, tone: 'b', ratio: '4 / 5', fit: 'contain' },
          { fig: '28', src: dancerRef3, tone: 'c', ratio: '4 / 5', fit: 'contain' },
        ],
      },
      {
        id: 'dancers-model',
        label: 'Dancing figurines — model',
        cols: 2,
        figs: [
          { fig: '29', src: dancerWhite, caption: 'White model', tone: 'b', ratio: '16 / 10' },
          { fig: '30', src: dancerTextured, caption: 'Textured model', tone: 'c', ratio: '16 / 10' },
        ],
      },
      {
        id: 'jade-suit',
        label: 'Jade burial suit',
        cols: 1,
        figs: [
          {
            fig: '31',
            src: jadeSuitRef,
            caption: 'Reference',
            tone: 'a',
            ratio: '2.75 / 1',
            fit: 'contain',
          },
        ],
      },
    ],
  },
  {
    id: '03',
    title: '#3 Interaction Design',
    tag: '03 / Interaction',
    reverse: false,
    groups: [
      {
        id: 'interaction',
        cols: 1,
        figs: [
          { fig: '32', caption: 'Placeholder — interaction still', tone: 'b', ratio: '16 / 10' },
        ],
      },
    ],
  },
  {
    id: '04',
    title: '#4 Technical Implementation',
    tag: '04 / Technical',
    reverse: true,
    groups: [
      {
        id: 'technical',
        cols: 1,
        figs: [
          { fig: '33', caption: 'Placeholder — technical notes', tone: 'a', ratio: '4 / 3' },
        ],
      },
    ],
  },
  {
    id: '05',
    title: '#5 Final Demo',
    tag: '05 / Demo',
    reverse: false,
    groups: [
      {
        id: 'demo',
        cols: 1,
        figs: [
          { fig: '34', caption: 'Placeholder — experience recording', tone: 'c', ratio: '16 / 9' },
        ],
      },
    ],
  },
]
</script>

<template>
  <section id="how" class="how" aria-labelledby="how-heading">
    <div class="how__header grid-12">
      <div class="how__index">
        <span class="meta-label">Section</span>
        <p class="how__num">03</p>
      </div>
      <div class="how__heading-wrap">
        <hr class="hairline how__rule" />
        <h2 id="how-heading" class="how__heading">How I Made It</h2>
      </div>
    </div>

    <article
      v-for="(step, index) in steps"
      :key="step.id"
      class="how__entry"
      :class="{ 'how__entry--last': index === steps.length - 1 }"
    >
      <hr class="hairline section-shell" />
      <div
        class="grid-12 how__row"
        :class="{ 'how__row--reverse': step.reverse }"
      >
        <div class="how__text">
          <p class="how__tag meta-label">{{ step.tag }}</p>
          <h3 class="how__sub">{{ step.title }}</h3>
        </div>
        <div class="how__media">
          <div v-for="group in step.groups" :key="group.id" class="how__group">
            <p v-if="group.label" class="how__group-label meta-label">
              {{ group.label }}
            </p>
            <div class="how__figs" :class="`how__figs--c${group.cols}`">
              <MediaPlaceholder
                v-for="item in group.figs"
                :key="item.fig"
                :fig="item.fig"
                :src="item.src"
                :caption="item.caption"
                :ratio="item.ratio"
                :tone="item.tone"
                :fit="item.fit || 'cover'"
              />
            </div>
          </div>
        </div>
      </div>
    </article>
  </section>
</template>

<style scoped>
.how {
  padding-block: clamp(3.5rem, 8vw, 6.5rem) clamp(4rem, 10vw, 8rem);
}

.how__header {
  align-items: end;
  margin-bottom: clamp(2rem, 4vw, 3rem);
}

.how__index {
  grid-column: 1 / span 2;
}

.how__num {
  margin-top: 0.35rem;
  font-size: clamp(1.5rem, 3vw, 2rem);
  letter-spacing: 0.08em;
  color: var(--bronze);
}

.how__heading-wrap {
  grid-column: 3 / span 10;
}

.how__rule {
  margin-bottom: 1.1rem;
}

.how__heading {
  font-size: clamp(1.25rem, 2.4vw, 1.75rem);
  font-weight: 400;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text);
}

.how__entry {
  padding-block: clamp(2.5rem, 5vw, 4rem);
}

.how__entry--last {
  padding-bottom: 0;
}

.how__row {
  padding-block: clamp(1.5rem, 3vw, 2.5rem) 0;
  align-items: start;
}

.how__text {
  grid-column: 1 / span 4;
  padding-top: 0.5rem;
}

.how__media {
  grid-column: 6 / span 7;
}

.how__row--reverse .how__text {
  grid-column: 9 / span 4;
}

.how__row--reverse .how__media {
  grid-column: 1 / span 7;
  order: -1;
}

.how__tag {
  margin-bottom: 0.85rem;
}

.how__sub {
  font-size: var(--lead);
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--text);
  margin-bottom: 1.1rem;
}

.how__group + .how__group {
  margin-top: clamp(1.75rem, 3.5vw, 2.75rem);
}

.how__group-label {
  margin-bottom: 0.7rem;
  color: var(--earth);
}

.how__figs {
  display: grid;
  gap: var(--gap);
  align-items: start;
}

.how__figs--c1 {
  grid-template-columns: minmax(0, 1fr);
}

.how__figs--c2 {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.how__figs--c3 {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

@media (max-width: 960px) {
  .how__index {
    grid-column: 1 / span 3;
  }

  .how__heading-wrap {
    grid-column: 4 / -1;
  }

  .how__text,
  .how__media,
  .how__row--reverse .how__text,
  .how__row--reverse .how__media {
    grid-column: 1 / -1;
    order: initial;
  }

  .how__media {
    margin-top: 1.5rem;
  }
}

@media (max-width: 600px) {
  .how__figs--c2 {
    grid-template-columns: minmax(0, 1fr);
  }

  .how__figs--c3 {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}
</style>
