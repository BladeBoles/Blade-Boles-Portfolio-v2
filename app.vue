<template>
  <nav class="portfolio__navbar--small">
    <button
      @click="toggleNav"
      class="portfolio__nav-toggle"
      aria-label="Toggle navigation"
    >
      <fa-bars />
    </button>
    <ul v-if="navOpen" class="portfolio__navlist--dropdown">
      <li class="portfolio__navlist-item">
        <button
          @click="toggleNav"
          class="portfolio__nav-close"
          aria-label="Toggle navigation"
        >
          <close-rounded />
        </button>
      </li>
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
  <nav class="portfolio__navbar">
    <ul class="portfolio__navlist">
      <li class="portfolio__navlist-item">
        <a class="portfolio__navlist-anchor" href="#">Home</a>
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
    <i class="fa-solid fa-c"></i>
    <section
      class="portfolio__section portfolio__section--greeting"
      id="portfolio__greeting"
    >
      <h1>Hello, world!</h1>
      <h2 class="portfolio__name-header">
        I'm <span class="portfolio__name-span">Blade</span>.
      </h2>
      <p class="portfolio__personal-headline">
        I'm a full stack developer. I really like JavaScript and TypeScript.
      </p>
    </section>
    <section class="portfolio__section" id="portfolio__bio">
      <h2 class="portfolio__section-header">About Me</h2>
      <div class="portfolio__section-bio">
        <div class="portfolio__section-bio-left">
          <img
            src="./assets/headshot.jpg"
            alt="A picture of Blade"
            class="portfolio__bio-headshot"
          />
        </div>
        <div class="portfolio__section-bio-right">
          <p class="portfolio__section-paragraph">
            I've been working as a full stack developer for the last 3 years.
            Before that I was a chemist who dreamt of developing software
            professionally. Coding makes me feel like a wizard, and my 5 year
            plan is to become Gandalf. The beard might take a little longer.
          </p>
          <p class="portfolio__section-paragraph">
            When I'm not writing code I'm gaming, reading, struggling to ride a
            snowboard, or adventuring with my partner and our Shiba Inu. I
            believe that the two most important things for a person to have are
            a sense of humor and a sense of purpose.
          </p>
        </div>
      </div>
    </section>
    <section class="portfolio__section" id="portfolio__projects">
      <h2 class="portfolio__section-header">Completed Projects</h2>
      <div class="portfolio__section-projects">
        <p class="portfolio__section-paragraph">
          I removed all of my old portfolio projects because they no longer
          reflect my skill level. Check back in the near future to see what I've
          been working on in my spare time.
        </p>
        <p class="portfolio__section-paragraph">
          Feel free to contact me to hear more about my professional experience
          or the side projects I have that aren't ready to release yet. You can
          also check out my
          <a
            href="https://github.com/BladeBoles/"
            class="portfolio__github-link"
            target="_blank"
            >GitHub</a
          >
          to get an idea of what I've been up to.
        </p>
      </div>
    </section>
    <footer class="portfolio__section" id="portfolio__contact">
      <ul class="portfolio__footer">
        <li class="portfolio__footer--email">
          <span class="portfolio__footer--email-span">Email: </span>
          <a
            class="portfolio__footer--email-link"
            href="mailto:bladerboles@gmail.com"
            >bladerboles@gmail.com</a
          >
        </li>
        <li class="portfolio__footer--socials">
          <a target="_blank" href="https://github.com/BladeBoles/"
            ><img
              class="portfolio__footer--gh-image"
              src="./assets/GitHub-Mark-Light-64px.png"
              alt=""
          /></a>

          <a target="_blank" href="https://www.linkedin.com/in/blade-boles/"
            ><img
              class="portfolio__footer--li-image"
              src="./assets/In-White-128-Γäó@2x.png"
              alt=""
          /></a>
        </li>
      </ul>
    </footer>
  </main>
</template>
<script setup>
import { ref } from 'vue'
import FaBars from '~icons/fa6-solid/bars'
import CloseRounded from '~icons/material-symbols/close-rounded'
useHead({
  link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]
})
const navOpen = ref(false)

const toggleNav = () => (navOpen.value = !navOpen.value)
</script>
<style>
* {
  font-family: roboto-slab;
}
body {
  background-color: #150811;
  color: #e3dbdb;
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

.portfolio__personal-headline {
  text-align: center;
}

.portfolio__nav-toggle {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 10000;
  background-color: inherit;
  color: inherit;
  font-size: 40px;
  border: none;
  margin-right: 10px;
}

.portfolio__nav-close {
  color: inherit;
  font-size: 28px;
  background-color: transparent;
  border: none;
  align-self: flex-end;
  margin-right: -5px;
  padding: 0;
}

.portfolio__nav-close:hover {
  color: #d1462f;
}

.portfolio__section-header {
  padding-top: 15vh;
}

.portfolio__navlist--dropdown {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  position: fixed;
  top: 0;
  right: 0;
  z-index: 10000;
  background-color: #150811;
  padding: 0;
}

.portfolio__navbar,
.portfolio__navbar--small {
  position: fixed;
  top: 0;
  height: 64px;
  width: 100vw;
  text-align: center;
  vertical-align: middle;
  z-index: 9999;
  background-color: #150811;
}

.portfolio__navbar--small {
  height: 64px;
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
  color: inherit;
  text-decoration: 2px #d1462f underline;
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
  font-size: 22px;
  color: inherit;
  background-color: inherit;
  border: 3px solid #355834;
  padding: 10px 20px;
}

.portfolio__work-button-anchor {
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  font-style: none;
  text-decoration: none;
}
.portfolio__work-button-anchor:hover {
  color: inherit;
  text-decoration: 3px solid #355834 underline;
}

.portfolio__section-paragraph {
  max-width: 600px;
  line-height: 150%;
}

.portfolio__section-bio {
  margin-top: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.portfolio__section-bio-right {
  align-self: flex-start;
}

.portfolio__bio-headshot {
  max-width: 350px;
  margin-right: 10vw;
}

.portfolio__section-projects {
  margin-top: 50px;
  max-width: 90vw;
}

.portfolio__github-link {
  color: inherit;
}
.portfolio__github-link:hover {
  color: #d1462f;
  text-decoration: 2px #d1462f underline;
}
.portfolio__footer {
  width: 80%;
  display: flex;
  flex-direction: column;
  list-style-type: none;
  margin: 0;
  padding: 0;
  font-size: 22px;
  justify-content: center;
  align-items: center;
}

.portfolio__footer--email-span {
  color: #d1462f;
}

.portfolio__footer--email-link {
  color: inherit;
  text-decoration: 2px #e3dbdb underline;
}

.portfolio__footer--email-link:hover {
  color: inherit;
}

.portfolio__footer--socials {
  display: flex;
  margin: 30px 0;
  width: 100%;
  justify-content: center;
  align-items: center;
}

.portfolio__footer--gh-image {
  margin-right: 30px;
}

.portfolio__footer--gh-image,
.portfolio__footer--li-image {
  width: 64px;
}

@media (min-width: 700px) {
  .portfolio__navbar--small {
    visibility: hidden;
  }
  .portfolio__nav-toggle {
    visibility: hidden;
  }
}

@media (max-width: 699px) {
  .portfolio__navbar {
    visibility: hidden;
  }
  .portfolio__section-bio {
    flex-direction: column;
  }
  .portfolio__section-bio-right {
    align-self: center;
    margin-top: 15px;
    max-width: 90vw;
  }
  .portfolio__bio-headshot {
    margin-right: 0;
  }
  .portfolio__section-header {
    padding-top: 20vh;
  }
}
</style>
