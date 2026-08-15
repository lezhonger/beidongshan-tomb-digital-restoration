<script setup>
import MediaPlaceholder from './MediaPlaceholder.vue'

const steps = [
  {
    id: '01',
    title: '#1 Research & Reference',
    tag: '01 / Research',
    reverse: false,
    figs: [
      { fig: '08', caption: 'Placeholder — research material', tone: 'a', ratio: '16 / 10' },
      { fig: '09', caption: 'Placeholder — site documentation', tone: 'b', ratio: '4 / 3' },
    ],
  },
  {
    id: '02',
    title: '#2 Building the Space',
    tag: '02 / Space',
    reverse: true,
    figs: [
      { fig: '10', caption: 'Placeholder — modelling process', tone: 'c', ratio: '16 / 9' },
      { fig: '11', caption: 'Placeholder — materials & lighting', tone: 'a', ratio: '4 / 3' },
    ],
  },
  {
    id: '03',
    title: '#3 Interaction Design',
    tag: '03 / Interaction',
    reverse: false,
    figs: [
      { fig: '12', caption: 'Placeholder — interaction still', tone: 'b', ratio: '16 / 10' },
    ],
  },
  {
    id: '04',
    title: '#4 Technical Implementation',
    tag: '04 / Technical',
    reverse: true,
    figs: [
      { fig: '13', caption: 'Placeholder — technical notes', tone: 'a', ratio: '4 / 3' },
    ],
  },
  {
    id: '05',
    title: '#5 Final Demo',
    tag: '05 / Demo',
    reverse: false,
    figs: [
      { fig: '14', caption: 'Placeholder — experience recording', tone: 'c', ratio: '16 / 9' },
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
          <p class="how__pending meta-label">Content forthcoming</p>
        </div>
        <div class="how__media">
          <div
            class="how__figs"
            :class="{ 'how__figs--pair': step.figs.length > 1 }"
          >
            <MediaPlaceholder
              v-for="item in step.figs"
              :key="item.fig"
              :fig="item.fig"
              :caption="item.caption"
              :ratio="item.ratio"
              :tone="item.tone"
            />
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

.how__pending {
  color: var(--earth);
}

.how__figs {
  display: flex;
  flex-direction: column;
  gap: var(--gap);
}

.how__figs--pair {
  display: grid;
  grid-template-columns: 1.35fr 1fr;
  gap: var(--gap);
  align-items: start;
}

.how__figs--pair > :last-child {
  margin-top: 1.75rem;
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

  .how__figs--pair {
    grid-template-columns: 1fr;
  }

  .how__figs--pair > :last-child {
    margin-top: 0;
  }
}
</style>
