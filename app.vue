<template>
  <nav
    id="portfolio__navbar"
    class="navbar navbar-expand-md navbar-dark bg-dark px-3"
  >
    <a class="navbar-brand" href="#">BB</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarScroll"
      aria-controls="navbarScroll"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarScroll">
      <ul
        class="nav-pills navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll nav"
        style="--bs-scroll-height: 100px"
      >
        <li class="nav-item">
          <a class="nav-link" href="#portfolio__greeting">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#portfolio__bio">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#portfolio__projects">Projects</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#portfolio__contact">Contact</a>
        </li>
      </ul>
    </div>
  </nav>
  <main
    data-bs-spy="scroll"
    tabindex="0"
    data-bs-offset="0"
    data-bs-target="#portfolio__navbar"
    class="portfolio__main"
  >
    <section id="portfolio__greeting">
      <h1>Hello, World!</h1>
      <h2>I'm <span>Blade</span>.</h2>
      <p>
        I write code and live in Boulder, CO. I enjoy full stack JavaScript and
        TypeScript development.
      </p>
      <button>View Work</button>
    </section>
    <section id="portfolio__bio">
      <h2>About Me</h2>
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
    <section id="portfolio__projects">
      <h2>Completed Projects:</h2>
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
    <footer id="portfolio__contact">
      <ul>
        <li>Email</li>
        <li>Phone</li>
        <li>LinkedIn</li>
      </ul>
    </footer>
  </main>
</template>

<style scoped>
.portfolio__main {
  position: relative;
}
</style>
