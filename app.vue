<template>
  <nav class="portfolio__navbar">
    <!-- <a class="navbar-brand" href="#">BB</a>
    <button
      aria-label="Toggle navigation"
    >
      <span>Toggle Icon</span>
    </button> -->
    <ul class="portfolio__navlist">
      <li class="portfolio__navlist-item">
        <a class="portfolio__navlist-anchor" href="#portfolio__greeting"
          >Home</a
        >
      </li>
      <li class="portfolio__navlist-item">
        <a class="portfolio__navlist-anchor" href="#portfolio__bio">About</a>
      </li>
      <li class="portfolio__navlist-item">
        <a class="portfolio__navlist-anchor" href="#portfolio__projects"
          >Projects</a
        >
      </li>
      <li class="portfolio__navlist-item">
        <a class="portfolio__navlist-anchor" href="#portfolio__contact"
          >Contact</a
        >
      </li>
    </ul>
  </nav>
  <main class="portfolio__main">
    <section
      class="portfolio__section portfolio__section--greeting"
      id="portfolio__greeting"
    >
      <h1>Hello, world!</h1>
      <h2 class="portfolio__name-header">
        I'm <span class="portfolio__name-span">Blade</span>.
      </h2>
      <p>I like full stack TypeScript development.</p>
      <button class="portfolio__work-button">View Work</button>
    </section>
    <section class="portfolio__section" id="portfolio__bio">
      <h2 class="portfolio__section-header">About Me</h2>
      <p>
        I've been working as a full stack developer for the last 3 years. Before
        that I was a chemist who dreamt of developing software. Coding makes me
        feel like a wizard, and my 5 year plan revolves around becoming Gandalf.
        The beard might take a little longer.
      </p>
      <p>
        When I'm not writing code I'm gaming, reading, struggling to ride a
        snowboard or adventuring with my partner and our Shiba Inu. I believe
        that a sense of humor and a sense of purpose are two of the most
        important things a person can have in life.
      </p>
    </section>
    <section class="portfolio__section" id="portfolio__projects">
      <h2 class="portfolio__section-header">Completed Projects:</h2>
      <p>
        I removed all of my old portfolio projects because they no longer
        reflect my skill level. Over the last couple of months I've been working
        on some really fun projects after work. Be sure to check back in the
        near future to see what I've been up to.
      </p>
      <p>
        Feel free to <button>Contact Me</button> to hear about my professional
        experience or the side projects I've been working on.
      </p>
    </section>
    <footer class="portfolio__section" id="portfolio__contact">
      <ul>
        <li>Email</li>
        <li>Phone</li>
        <li>LinkedIn</li>
      </ul>
    </footer>
  </main>
</template>

<style>
body {
  background-color: #150811;
  color: #e3dbdb;
  font-family: roboto-slab;
}

p {
  font-size: 22px;
}

section {
  min-height: 100vh;
}

h1 {
  padding-top: 15vh;
}

.portfolio__section-header {
  padding-top: 15vh;
}

.portfolio__navbar {
  position: fixed;
  top: 0;
  height: 15vh;
  width: 100vw;
  text-align: center;
  vertical-align: middle;
  z-index: 9999;
  background-color: #150811;
}

.portfolio__navlist {
  position: absolute;
  top: 25%;
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100%;
}

.portfolio__navlist-item {
  display: inline;
  margin: 0 5%;
}

.portfolio__navlist-anchor {
  text-decoration: none;
  color: inherit;
  font-size: 22px;
}

.portfolio__navlist-anchor:hover {
  color: #d1462f;
}

.portfolio__section--greeting {
  justify-content: center;
  margin-top: -15vh;
}

.portfolio__section {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.portfolio__name-header {
  margin: 20px 0;
}

.portfolio__name-span {
  color: #d1462f;
  font-weight: 500;
}

.portfolio__work-button {
  color: inherit;
  background-color: inherit;
  border: 3px solid #d1462f;
  padding: 10px 20px;
}
</style>
