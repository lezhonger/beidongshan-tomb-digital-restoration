<script setup>
import MediaPlaceholder from './MediaPlaceholder.vue'
</script>

<template>
  <section class="hero" aria-label="Project introduction">
    <div class="hero__bg" aria-hidden="true">
      <MediaPlaceholder
        fig="00"
        tone="a"
        full-bleed
        breath
        class="hero__plane"
      />
      <div class="hero__scrim"></div>
    </div>

    <div class="hero__content grid-12">
      <div class="hero__copy">
        <h1 class="hero__title anim-fade-up d1">
          Reconstructing the<br />Underground World
        </h1>
        <p class="hero__subtitle anim-fade-up d2">
          A Digital Restoration of the Beidongshan Tomb from Han Dynasty
        </p>
        <p class="hero__brief anim-fade-up d3">
          A Unity-based immersive experience exploring how digital technology can
          preserve and reinterpret ancient cultural heritage.
        </p>
        <span class="dim-line hero__dim anim-fade-up d3" aria-hidden="true"></span>
      </div>

      <aside class="hero__meta anim-fade-up d4">
        <div class="hero__meta-block">
          <span class="meta-label">Location</span>
          <p>Xuzhou, Jiangsu, China</p>
        </div>
        <div class="hero__meta-block">
          <span class="meta-label">Classification</span>
          <p>Digital Heritage · Interactive Experience · Unity</p>
        </div>
        <div class="hero__meta-block">
          <span class="meta-label">Site Coord.</span>
          <p>34.26°N · 117.18°E</p>
        </div>
      </aside>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  min-height: calc(100vh - 2.75rem);
  display: flex;
  align-items: flex-end;
  overflow: hidden;
}

.hero__bg {
  position: absolute;
  inset: 0;
  z-index: 0;
}

.hero__plane {
  display: block;
  width: 100%;
  height: 100%;
}

.hero__plane :deep(.media),
.hero__plane :deep(.media__plane) {
  width: 100%;
  height: 100%;
  min-height: 100%;
  border: none;
}

/* Soft darkening so type stays readable on the image plane */
.hero__scrim {
  position: absolute;
  inset: 0;
  pointer-events: none;
  background:
    linear-gradient(
      to top,
      rgba(20, 18, 16, 0.82) 0%,
      rgba(20, 18, 16, 0.45) 42%,
      rgba(20, 18, 16, 0.18) 100%
    );
}

.hero__content {
  position: relative;
  z-index: 1;
  width: 100%;
  padding-block: clamp(2.5rem, 6vw, 4.5rem);
  align-items: end;
}

.hero__copy {
  grid-column: 1 / span 7;
  max-width: 38rem;
}

.hero__kicker {
  margin-bottom: 1rem;
}

.hero__title {
  font-size: clamp(1.75rem, 4.2vw, 3.25rem);
  font-weight: 400;
  line-height: 1.15;
  letter-spacing: -0.02em;
  color: var(--text);
}

.hero__subtitle {
  margin-top: 1.1rem;
  font-size: var(--lead);
  line-height: 1.55;
  color: var(--muted);
  max-width: 32rem;
}

.hero__brief {
  margin-top: 1.35rem;
  font-size: var(--body);
  line-height: 1.7;
  color: var(--text);
  max-width: 30rem;
  opacity: 0.92;
}

.hero__dim {
  margin-top: 1.75rem;
  max-width: 12rem;
}

.hero__meta {
  grid-column: 9 / span 4;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  padding-bottom: 0.25rem;
  border-left: 1px solid var(--line-strong);
  padding-left: 1.25rem;
}

.hero__meta-block p {
  margin-top: 0.35rem;
  font-size: var(--caption);
  letter-spacing: 0.04em;
  color: var(--text);
  line-height: 1.5;
}

@media (max-width: 960px) {
  .hero__copy {
    grid-column: 1 / -1;
  }

  .hero__meta {
    grid-column: 1 / -1;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 1.5rem 2rem;
    margin-top: 1.75rem;
    border-left: none;
    border-top: 1px solid var(--line-strong);
    padding-left: 0;
    padding-top: 1.25rem;
  }

  .hero__meta-block {
    flex: 1 1 10rem;
  }
}

@media (max-width: 600px) {
  .hero__title br {
    display: none;
  }
}
</style>
