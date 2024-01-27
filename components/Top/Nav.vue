<script setup>
const name = ref("NAWIGACJA");
</script>
<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="https://bulma.io">
        <img
          src="https://bulma.io/images/bulma-logo.png"
          width="112"
          height="28"
        />
      </a>

      <a
        role="button"
        class="navbar-burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item"> Home </a>

        <a class="navbar-item"> Documentation </a>

        <div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link"> More </a>

          <div class="navbar-dropdown">
            <a class="navbar-item"> About </a>
            <a class="navbar-item"> Jobs </a>
            <a class="navbar-item"> Contact </a>
            <hr class="navbar-divider" />
            <a class="navbar-item"> Report an issue </a>
          </div>
        </div>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-primary">
              <strong>Sign up</strong>
            </a>
            <a class="button is-light"> Log in </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
  <div id="navsec">
    <h1 id="main">{{ name }}</h1>
    <ul>
      <li><NuxtLink to="/">Strona główna</NuxtLink></li>
      <li><nuxt-link to="/about">O nas (SPA)</nuxt-link></li>
      <li class="mpa"><a href="/about">O nas (MPA)</a></li>
      <li><nuxt-link to="/articles/1">Artykuł 1</nuxt-link></li>
      <li><nuxt-link to="/articles/2">Artykuł 2</nuxt-link></li>
    </ul>
  </div>
</template>
<style scoped lang="scss">
h1 {
  color: red;
}

ul {
  .mpa {
    color: yellow;
  }
}
</style>
