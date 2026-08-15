<template>
  <header class="archive-bar">
    <div class="archive-bar__inner section-shell">
      <div class="archive-bar__left">
        <span class="meta-label">Archive</span>
        <span class="sep">/</span>
        <span>Beidongshan</span>
        <span class="sep">/</span>
        <span>Western Han</span>
      </div>
      <div class="archive-bar__right">
        <span>34.26°N 117.18°E</span>
        <span class="sep">·</span>
        <span>Digital Heritage</span>
      </div>
    </div>
    <hr class="hairline" />
  </header>
</template>

<style scoped>
.archive-bar {
  position: sticky;
  top: 0;
  z-index: 20;
  background: var(--bg);
}

.archive-bar__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  min-height: 2.75rem;
  font-size: var(--caption);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--muted);
}

.archive-bar__left,
.archive-bar__right {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.45rem;
}

.sep {
  color: var(--earth);
}

@media (max-width: 720px) {
  .archive-bar__right {
    display: none;
  }
}
</style>
