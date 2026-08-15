<script setup>
import MediaPlaceholder from './MediaPlaceholder.vue'
</script>

<template>
  <section id="why" class="why" aria-labelledby="why-heading">
    <div class="why__header grid-12">
      <div class="why__index">
        <span class="meta-label">Section</span>
        <p class="why__num">01</p>
      </div>
      <div class="why__heading-wrap">
        <hr class="hairline why__rule" />
        <h2 id="why-heading" class="why__heading">Why Did I Do It?</h2>
      </div>
    </div>

    <!-- Entry 01: Personal Interest -->
    <article class="why__entry">
      <hr class="hairline section-shell" />
      <div class="grid-12 why__row">
        <div class="why__text why__text--a">
          <p class="why__tag meta-label">01 / Motive</p>
          <h3 class="why__sub"># Personal Interest</h3>
          <p class="why__body">
            Having a keen interest in history and cultural relics, I once traveled
            to Egypt and witnessed historic sites such as the pyramids, which also
            sparked my curiosity about China’s history and cultural heritage.
          </p>
        </div>
        <div class="why__media why__media--a">
          <MediaPlaceholder
            fig="01"
            caption="Egypt travel photograph — field note"
            ratio="4 / 3"
            tone="b"
          />
        </div>
      </div>
    </article>

    <!-- Entry 02: Cultural Heritage Context -->
    <article class="why__entry">
      <hr class="hairline section-shell" />
      <div class="grid-12 why__row why__row--b">
        <div class="why__media why__media--b">
          <div class="why__gallery">
            <MediaPlaceholder
              fig="02"
              caption="Xuzhou location map"
              ratio="16 / 10"
              tone="a"
              class="why__gal-main"
            />
            <MediaPlaceholder
              fig="03"
              caption="Han tomb, Xuzhou"
              ratio="4 / 3"
              tone="c"
              class="why__gal-side"
            />
            <MediaPlaceholder
              fig="04"
              caption="Beidongshan site"
              ratio="4 / 3"
              tone="b"
              class="why__gal-side"
            />
          </div>
        </div>
        <div class="why__text why__text--b">
          <p class="why__tag meta-label">02 / Context</p>
          <h3 class="why__sub"># The Cultural Heritage Context</h3>
          <p class="why__body">
            Xuzhou, in Jiangsu Province, is home to many tombs of vassal kings from
            the Han Dynasty. The city of Xuzhou in Jiangsu Province is home to
            numerous tombs of Han-dynasty feudal princes. These tombs are of a very
            high rank, featuring large areas and spacious interiors, and contain a
            great number of burial objects.
          </p>
        </div>
      </div>
    </article>

    <!-- Entry 03: Why Digital Preservation? -->
    <article class="why__entry why__entry--last">
      <hr class="hairline section-shell" />
      <div class="grid-12 why__row">
        <div class="why__text why__text--c">
          <p class="why__tag meta-label">03 / Preservation</p>
          <h3 class="why__sub"># Why Digital Preservation?</h3>
          <p class="why__body">
            In modern society, the preservation of cultural relics is of great
            importance. Natural disasters, armed conflicts, accidents, and urban
            development can all impact and damage historical relics and
            archaeological sites. Examples include the destruction of the Bamiyan
            Buddhas by dynamite carried out by extremist organizations in 2001, and
            the fire that devastated Notre-Dame de Paris in 2019—events that have
            caused immense regret and sorrow. This has inspired me to consider using
            modern technological methods to restore historical relics.
          </p>
        </div>
        <aside class="why__note" aria-label="Archive annotation">
          <span class="meta-label">Annotation</span>
          <p>Cases referenced</p>
          <ul>
            <li>Bamiyan Buddhas — 2001</li>
            <li>Notre-Dame de Paris — 2019</li>
          </ul>
          <span class="dim-line why__note-line" aria-hidden="true"></span>
          <p class="why__note-foot">Digital record as secondary preservation</p>
        </aside>
      </div>
    </article>
  </section>
</template>

<style scoped>
.why {
  padding-block: clamp(3.5rem, 8vw, 6.5rem) clamp(4rem, 10vw, 8rem);
}

.why__header {
  align-items: end;
  margin-bottom: clamp(2rem, 4vw, 3rem);
}

.why__index {
  grid-column: 1 / span 2;
}

.why__num {
  margin-top: 0.35rem;
  font-size: clamp(1.5rem, 3vw, 2rem);
  letter-spacing: 0.08em;
  color: var(--bronze);
}

.why__heading-wrap {
  grid-column: 3 / span 10;
}

.why__rule {
  margin-bottom: 1.1rem;
}

.why__heading {
  font-size: clamp(1.25rem, 2.4vw, 1.75rem);
  font-weight: 400;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text);
}

.why__entry {
  padding-block: clamp(2.5rem, 5vw, 4rem);
}

.why__entry--last {
  padding-bottom: 0;
}

.why__row {
  padding-block: clamp(1.5rem, 3vw, 2.5rem) 0;
  align-items: start;
}

.why__tag {
  margin-bottom: 0.85rem;
}

.why__sub {
  font-size: var(--lead);
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--text);
  margin-bottom: 1.1rem;
}

.why__body {
  font-size: var(--body);
  line-height: 1.8;
  color: var(--muted);
  max-width: 36rem;
}

.why__text--a {
  grid-column: 1 / span 5;
  padding-top: 0.5rem;
}

.why__media--a {
  grid-column: 7 / span 6;
}

.why__media--b {
  grid-column: 1 / span 7;
}

.why__text--b {
  grid-column: 9 / span 4;
  padding-top: 0.25rem;
}

.why__text--b .why__body {
  max-width: none;
}

.why__text--c {
  grid-column: 2 / span 7;
}

.why__note {
  grid-column: 10 / span 3;
  border-left: 1px solid var(--line);
  padding-left: 1.1rem;
  color: var(--muted);
  font-size: var(--caption);
  letter-spacing: 0.04em;
}

.why__note p {
  margin-top: 0.5rem;
  color: var(--text);
}

.why__note ul {
  list-style: none;
  margin-top: 0.85rem;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}

.why__note-line {
  margin-block: 1.25rem 1rem;
}

.why__note-foot {
  color: var(--earth) !important;
  line-height: 1.5;
}

.why__gallery {
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  grid-template-rows: auto auto;
  gap: var(--gap);
}

.why__gal-main {
  grid-column: 1 / -1;
}

.why__gal-side:nth-child(2) {
  margin-top: 1.5rem;
}

@media (max-width: 960px) {
  .why__index {
    grid-column: 1 / span 3;
  }

  .why__heading-wrap {
    grid-column: 4 / -1;
  }

  .why__text--a,
  .why__media--a,
  .why__media--b,
  .why__text--b,
  .why__text--c,
  .why__note {
    grid-column: 1 / -1;
  }

  .why__media--a,
  .why__media--b {
    margin-top: 1.5rem;
  }

  .why__text--b {
    order: -1;
  }

  .why__row--b {
    display: flex;
    flex-direction: column;
  }

  .why__note {
    margin-top: 2rem;
    border-left: none;
    border-top: 1px solid var(--line);
    padding-left: 0;
    padding-top: 1.25rem;
  }
}

@media (max-width: 600px) {
  .why__gallery {
    grid-template-columns: 1fr;
  }

  .why__gal-side:nth-child(2) {
    margin-top: 0;
  }
}
</style>
