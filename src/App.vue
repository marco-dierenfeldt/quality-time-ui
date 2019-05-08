<template>
  <div class="container-fluent">
    <nav class="navbar navbar-expand-md navbar-dark bg-dark fixed-top">
      <a class="navbar-brand" href="#">QualityTime!</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExampleDefault"
              aria-controls="navbarsExampleDefault" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarsExampleDefault">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item"  :class="{active: currentPage == 'Home'}" @click="currentPage='Home'">
            <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item" :class="{active: currentPage == 'About'}" @click="currentPage='About'">
            <router-link class="nav-link" to="/about">About</router-link>
          </li>
        </ul>
    </div>
    </nav>

    <main role="main" class="container">
      <div class="starter-template">
        <router-view/>
      </div>

    </main><!-- /.container -->
  </div>
</template>

<script>
  export default {
      data() {
          return {
              currentPage: 'Home'
          }
      }
  }
</script>

<style>

</style>
