<script setup>
import MediaPlaceholder from './MediaPlaceholder.vue'
</script>

<template>
  <section id="beyond" class="beyond" aria-labelledby="beyond-heading">
    <div class="beyond__header grid-12">
      <div class="beyond__index">
        <span class="meta-label">Section</span>
        <p class="beyond__num">04</p>
      </div>
      <div class="beyond__heading-wrap">
        <hr class="hairline beyond__rule" />
        <h2 id="beyond-heading" class="beyond__heading">Beyond This Project</h2>
      </div>
    </div>

    <article class="beyond__entry">
      <hr class="hairline section-shell" />
      <div class="grid-12 beyond__row">
        <div class="beyond__text">
          <p class="beyond__tag meta-label">01 / Method</p>
          <h3 class="beyond__sub"># Digital Preservation</h3>
          <p class="beyond__body">
            Although this project focuses on one Han Dynasty tomb, its methods can
            be applied to cultural heritage sites throughout the world.
            Archaeological sites, historic buildings, religious structures,
            monuments, museum collections, and entire historic neighbourhoods can
            be digitally recorded and reconstructed. This is especially valuable
            when physical sites are threatened by natural disasters, warfare,
            climate change, erosion, vandalism, urban expansion, or the gradual
            deterioration of materials.
          </p>
          <p class="beyond__body beyond__body--follow">
            Digital reconstruction does not replace the preservation of the
            original site. Instead, it creates an additional record that can
            support research, education, conservation, and future restoration. A
            detailed 3D model can preserve information about a site’s scale,
            layout, materials, decoration, and relationship between objects. Even
            if the physical location later becomes damaged or inaccessible,
            researchers and members of the public may still be able to study its
            previous appearance.
          </p>
        </div>
        <aside class="beyond__aside">
          <MediaPlaceholder
            fig="15"
            caption="Method — transferable digital record"
            ratio="3 / 4"
            tone="b"
          />
          <div class="beyond__note">
            <span class="meta-label">Annotation</span>
            <p>Keywords</p>
            <ul>
              <li>Method</li>
              <li>Secondary record</li>
              <li>Conservation support</li>
            </ul>
          </div>
        </aside>
      </div>
    </article>

    <article class="beyond__entry">
      <hr class="hairline section-shell" />
      <div class="grid-12 beyond__row">
        <div class="beyond__text">
          <p class="beyond__tag meta-label">02 / Access</p>
          <h3 class="beyond__sub"># Accessibility &amp; Education</h3>
          <p class="beyond__body">
            The approach also has significant potential in the United States.
            American museums, universities, historical societies, preservation
            organisations, and local communities could use similar technology to
            document archaeological landscapes, historic buildings, monuments,
            industrial sites, and museum collections. Digital models could allow
            students to explore locations that would otherwise be too distant,
            fragile, expensive, or dangerous to visit physically.
          </p>
          <p class="beyond__body beyond__body--follow">
            For example, interactive reconstructions could be used to demonstrate
            how a historic building changed over time, return displaced artefacts
            to their original architectural context digitally, or compare different
            scholarly interpretations of an archaeological site. They could also
            improve accessibility for people with disabilities and for students who
            cannot travel to major museums or heritage locations.
          </p>
        </div>
        <aside class="beyond__note beyond__note--rail" aria-label="Archive annotation">
          <span class="meta-label">Annotation</span>
          <p>Keywords</p>
          <ul>
            <li>Access</li>
            <li>Education</li>
            <li>Remote learning</li>
          </ul>
          <span class="dim-line beyond__note-line" aria-hidden="true"></span>
          <p class="beyond__note-foot">Distance, fragility, cost, risk</p>
        </aside>
      </div>
    </article>

    <article class="beyond__entry beyond__entry--last">
      <hr class="hairline section-shell" />
      <div class="grid-12 beyond__row">
        <div class="beyond__text">
          <p class="beyond__tag meta-label">03 / Responsibility</p>
          <h3 class="beyond__sub"># Cultural Responsibility</h3>
          <p class="beyond__body">
            The technology could be particularly valuable when working with
            Indigenous and culturally sensitive heritage. However, these projects
            should be created in consultation with descendant communities, who
            should have authority over how culturally significant places and
            objects are represented. Some knowledge or locations may not be
            appropriate for unrestricted public display. Digital preservation
            should therefore combine technical accuracy with cultural
            responsibility.
          </p>
          <p class="beyond__body beyond__body--follow">
            More broadly, the project demonstrates that 3D modelling can connect
            cultural heritage with modern audiences. It can transform
            archaeological evidence into an experience that is understandable and
            engaging without reducing the complexity of the history. Through online
            platforms, virtual exhibitions, classroom resources, and museum
            installations, digital heritage projects can make the past accessible
            to audiences across different countries while encouraging greater
            awareness of the importance of preservation.
          </p>
        </div>
        <aside class="beyond__note beyond__note--rail" aria-label="Archive annotation">
          <span class="meta-label">Annotation</span>
          <p>Keywords</p>
          <ul>
            <li>Responsibility</li>
            <li>Community authority</li>
            <li>Public access</li>
          </ul>
          <span class="dim-line beyond__note-line" aria-hidden="true"></span>
          <p class="beyond__note-foot">Accuracy with cultural care</p>
        </aside>
      </div>
    </article>
  </section>
</template>

<style scoped>
.beyond {
  padding-block: clamp(3.5rem, 8vw, 6.5rem) clamp(5rem, 12vw, 9rem);
}

.beyond__header {
  align-items: end;
  margin-bottom: clamp(2rem, 4vw, 3rem);
}

.beyond__index {
  grid-column: 1 / span 2;
}

.beyond__num {
  margin-top: 0.35rem;
  font-size: clamp(1.5rem, 3vw, 2rem);
  letter-spacing: 0.08em;
  color: var(--bronze);
}

.beyond__heading-wrap {
  grid-column: 3 / span 10;
}

.beyond__rule {
  margin-bottom: 1.1rem;
}

.beyond__heading {
  font-size: clamp(1.25rem, 2.4vw, 1.75rem);
  font-weight: 400;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text);
}

.beyond__entry {
  padding-block: clamp(2.5rem, 5vw, 4rem);
}

.beyond__entry--last {
  padding-bottom: 0;
}

.beyond__row {
  padding-block: clamp(1.5rem, 3vw, 2.5rem) 0;
  align-items: start;
}

.beyond__tag {
  margin-bottom: 0.85rem;
}

.beyond__sub {
  font-size: var(--lead);
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--text);
  margin-bottom: 1.1rem;
}

.beyond__text {
  grid-column: 2 / span 7;
}

.beyond__body {
  font-size: var(--body);
  line-height: 1.8;
  color: var(--muted);
  max-width: 40rem;
}

.beyond__body--follow {
  margin-top: 1.1rem;
}

.beyond__aside {
  grid-column: 10 / span 3;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.beyond__note {
  color: var(--muted);
  font-size: var(--caption);
  letter-spacing: 0.04em;
}

.beyond__note--rail {
  grid-column: 10 / span 3;
  border-left: 1px solid var(--line);
  padding-left: 1.1rem;
}

.beyond__note p {
  margin-top: 0.5rem;
  color: var(--text);
}

.beyond__note ul {
  list-style: none;
  margin-top: 0.85rem;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}

.beyond__note-line {
  margin-block: 1.25rem 1rem;
}

.beyond__note-foot {
  color: var(--earth) !important;
  line-height: 1.5;
}

@media (max-width: 960px) {
  .beyond__index {
    grid-column: 1 / span 3;
  }

  .beyond__heading-wrap {
    grid-column: 4 / -1;
  }

  .beyond__text,
  .beyond__aside,
  .beyond__note--rail {
    grid-column: 1 / -1;
  }

  .beyond__aside,
  .beyond__note--rail {
    margin-top: 2rem;
  }

  .beyond__note--rail {
    border-left: none;
    border-top: 1px solid var(--line);
    padding-left: 0;
    padding-top: 1.25rem;
  }

  .beyond__aside {
    max-width: 18rem;
  }
}
</style>
