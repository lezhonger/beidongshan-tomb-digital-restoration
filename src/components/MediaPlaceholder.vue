<script setup>
defineProps({
  fig: {
    type: String,
    required: true,
  },
  caption: {
    type: String,
    default: '',
  },
  /** CSS aspect-ratio value, e.g. "16 / 9" or "4 / 3" */
  ratio: {
    type: String,
    default: '16 / 9',
  },
  /** placeholder tone: a | b | c */
  tone: {
    type: String,
    default: 'a',
    validator: (v) => ['a', 'b', 'c'].includes(v),
  },
  fullBleed: {
    type: Boolean,
    default: false,
  },
  breath: {
    type: Boolean,
    default: false,
  },
  /** Resolved image URL. When absent the tinted plane is shown instead. */
  src: {
    type: String,
    default: '',
  },
  alt: {
    type: String,
    default: '',
  },
  /** "contain" keeps drawings and plans uncropped; "cover" fills the plate */
  fit: {
    type: String,
    default: 'cover',
    validator: (v) => ['cover', 'contain'].includes(v),
  },
  /** Above-the-fold imagery: load eagerly instead of lazily */
  priority: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <figure
    class="media"
    :class="[
      `tone-${tone}`,
      { 'is-full': fullBleed, 'anim-breath': breath, 'has-img': !!src },
    ]"
  >
    <div class="media__plane" :style="{ aspectRatio: fullBleed ? undefined : ratio }">
      <img
        v-if="src"
        class="media__img"
        :style="{ objectFit: fit }"
        :src="src"
        :alt="alt || caption"
        :loading="priority ? 'eager' : 'lazy'"
        :fetchpriority="priority ? 'high' : 'auto'"
        decoding="async"
      />
      <span class="media__fig">FIG. {{ fig }}</span>
    </div>
    <figcaption v-if="caption" class="media__caption">{{ caption }}</figcaption>
  </figure>
</template>

<style scoped>
.media {
  margin: 0;
  min-width: 0;
}

.media__plane {
  position: relative;
  width: 100%;
  border: 1px solid var(--line);
  overflow: hidden;
}

.media.is-full .media__plane {
  aspect-ratio: auto;
  height: 100%;
  min-height: inherit;
  border: none;
  border-bottom: 1px solid var(--line);
}

.tone-a .media__plane {
  background: var(--placeholder-a);
}

.tone-b .media__plane {
  background: var(--placeholder-b);
}

.tone-c .media__plane {
  background: var(--placeholder-c);
}

.media__img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  max-width: none;
}

.media__fig {
  position: absolute;
  top: 0.65rem;
  left: 0.75rem;
  font-size: var(--caption);
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--bronze);
  pointer-events: none;
}

/* Many references are line drawings on white, so the label needs its own plate */
.has-img .media__fig {
  top: 0;
  left: 0;
  padding: 0.3rem 0.5rem;
  background: rgba(20, 18, 16, 0.72);
  color: var(--text);
}

/* Full-bleed imagery has no frame, so align the label to the page gutter */
.has-img.is-full .media__fig {
  top: 0.9rem;
  left: var(--gutter);
  padding: 0;
  background: none;
  color: var(--bronze);
}

.media__caption {
  margin-top: 0.55rem;
  font-size: var(--caption);
  letter-spacing: 0.06em;
  color: var(--muted);
  line-height: 1.4;
}

.anim-breath .media__plane {
  animation: breath 12s ease-in-out infinite;
}
</style>
