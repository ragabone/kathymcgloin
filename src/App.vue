<script setup>
import frontCover from './assets/Front Cover.png'

const navigation = [
  { label: 'The Book', href: '#book' },
  { label: 'Launch', href: '#launch' },
  { label: 'Author', href: '#author' },
  { label: 'Where to Buy', href: '#buy' },
]
</script>

<template>
  <header class="site-header">
    <a class="brand" href="#top" aria-label="Second Chances by the Sea home">
      <span>Second Chances</span>
      <small>by the Sea</small>
    </a>
    <nav aria-label="Main navigation">
      <a v-for="item in navigation" :key="item.href" :href="item.href">{{ item.label }}</a>
    </nav>
  </header>

  <main id="top">
    <section class="hero" aria-labelledby="hero-title">
      <div class="hero-copy">
        <p class="eyebrow">A novel by Kathy McGloin</p>
        <h1 id="hero-title">Second Chances<br /><em>by the Sea</em></h1>
        <p class="tagline">Sometimes the place you escape to becomes the place you finally belong.</p>
        <a class="button" href="#book">Discover the story <span aria-hidden="true">↓</span></a>
      </div>
      <div class="cover-wrap">
        <img class="cover-image" :src="frontCover" alt="Front cover of Second Chances by the Sea by Kathy McGloin" />
      </div>
    </section>

    <section id="book" class="section story-section" aria-labelledby="book-title">
      <div class="section-label">The story</div>
      <div>
        <h2 id="book-title">A new shore. A fresh start.</h2>
        <p class="lead">After a devastating betrayal shatters the life she thought she was building in Belfast, Erin escapes to the seaside town of Bundoran on Ireland’s west coast, hoping only for a fresh start and a little peace.</p>
        <p class="muted">Further synopsis text, genre, and themes will be added here.</p>
      </div>
    </section>

    <section id="launch" class="launch-section" aria-labelledby="launch-title">
      <div class="launch-intro">
        <p class="eyebrow">You’re invited</p>
        <h2 id="launch-title">Book launch</h2>
        <p>Join Kathy McGloin to celebrate <em>Second Chances by the Sea</em>.</p>
      </div>
      <div class="launch-details">
        <p class="date">Wednesday<br /><strong>September 9, 2026</strong></p>
        <p><strong>18:30</strong><br />Marc Geagan Suite<br />Bundoran Community Centre<br />Bundoran, County Donegal</p>
        <p class="refreshments">Refreshments served</p>
      </div>
    </section>

    <section id="author" class="section author-section" aria-labelledby="author-title">
      <div class="portrait-placeholder" role="img" aria-label="Author photograph placeholder">Author photo<br />to be added</div>
      <div>
        <div class="section-label">The author</div>
        <h2 id="author-title">Kathy McGloin</h2>
        <p class="lead">Author biography to be supplied.</p>
        <p class="muted">This space is ready for a short biography, author photograph, and any relevant links or news.</p>
      </div>
    </section>

    <section class="setting-section" aria-labelledby="setting-title">
      <div>
        <p class="eyebrow">The setting</p>
        <h2 id="setting-title">At the edge of the Atlantic</h2>
        <p>Bundoran, on Ireland’s west coast, and its striking Fairy Bridges form an important part of the novel’s coastal atmosphere.</p>
      </div>
      <div class="coast-art" role="img" aria-label="Coastal artwork placeholder for Bundoran and the Fairy Bridges">
        <span>Bundoran &amp; the Fairy Bridges</span>
        <small>Coastal artwork to be added</small>
      </div>
    </section>

    <section id="buy" class="section buy-section" aria-labelledby="buy-title">
      <div class="section-label">Find your copy</div>
      <div>
        <h2 id="buy-title">Where to buy</h2>
        <p class="lead">Purchase details will be announced soon.</p>
        <div class="buy-options">
          <div><strong>Local retailers</strong><span>Details to be added</span></div>
          <div><strong>Direct purchase</strong><span>Details to be added</span></div>
          <div><strong>Online bookshops</strong><span>Links to be added</span></div>
        </div>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <p><strong>Second Chances by the Sea</strong> &mdash; Kathy McGloin</p>
    <p>Contact and social links to be added.</p>
  </footer>
</template>
