<template>
  <header class="archive-bar">
    <nav class="archive-bar__inner section-shell" aria-label="Section navigation">
      <a href="#why" class="nav-link is-expandable" aria-label="Why Did I Do It?">
        <span>Why</span>
        <span class="nav-link__rest" aria-hidden="true">
          <span>&nbsp;Did I Do It?</span>
        </span>
      </a>
      <span class="sep">/</span>
      <a href="#what" class="nav-link is-expandable" aria-label="What Did I Do?">
        <span>What</span>
        <span class="nav-link__rest" aria-hidden="true">
          <span>&nbsp;Did I Do?</span>
        </span>
      </a>
      <span class="sep">/</span>
      <a href="#how" class="nav-link is-expandable" aria-label="How I Made It">
        <span>How</span>
        <span class="nav-link__rest" aria-hidden="true">
          <span>&nbsp;I Made It</span>
        </span>
      </a>
      <span class="sep">/</span>
      <a href="#beyond" class="nav-link">Beyond This Project</a>
    </nav>
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
  flex-wrap: wrap;
  align-items: center;
  justify-content: flex-end;
  gap: 0.45rem;
  min-height: 2.75rem;
  font-size: var(--caption);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--muted);
}

.nav-link {
  display: inline-flex;
  align-items: baseline;
  color: inherit;
  white-space: nowrap;
  transition: color 0.2s ease;
}

.nav-link:hover,
.nav-link:focus-visible {
  color: var(--text);
}

.nav-link__rest {
  display: grid;
  grid-template-columns: 0fr;
  transition: grid-template-columns 0.35s ease;
}

.nav-link__rest > span {
  overflow: hidden;
  min-width: 0;
  white-space: nowrap;
}

.nav-link.is-expandable:hover .nav-link__rest,
.nav-link.is-expandable:focus-visible .nav-link__rest {
  grid-template-columns: 1fr;
}

.sep {
  color: var(--earth);
}

@media (prefers-reduced-motion: reduce) {
  .nav-link__rest {
    transition: none;
  }
}
</style>
