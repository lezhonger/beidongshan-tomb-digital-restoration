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
})
</script>

<template>
  <figure
    class="media"
    :class="[`tone-${tone}`, { 'is-full': fullBleed, 'anim-breath': breath }]"
  >
    <div class="media__plane" :style="{ aspectRatio: fullBleed ? undefined : ratio }">
      <span class="media__fig">FIG. {{ fig }}</span>
      <!-- Replace this plane with <img> later -->
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
