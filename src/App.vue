<template>
  <div class="container">
    <header class="blog-header lh-1 py-3">
      <div class="row flex-nowrap justify-content-between align-items-center">
        <div class="col-4 pt-1">
          <!-- <a class="link-secondary" href="#">Subscribe</a> -->
        </div>
        <div class="col-4 text-center">
          <router-link class="blog-header-logo text-dark" to="/">Large</router-link>
        </div>
        <div class="col-4 d-flex justify-content-end align-items-center">
          <!-- <a class="link-secondary" href="#" aria-label="Search">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="mx-3" role="img" viewBox="0 0 24 24"><title>Search</title><circle cx="10.5" cy="10.5" r="7.5"></circle><path d="M21 21l-5.2-5.2"></path></svg>
          </a> -->
          <a class="btn btn-sm btn-outline-secondary" @click="$router.go(-1)">Back</a>
        </div>
      </div>
    </header>
    <div class="nav-scroller py-1 mb-2">
      <nav class="nav d-flex justify-content-between">
        <router-link class="p-2 link-secondary" to="/">Home</router-link>
        <router-link class="p-2 link-secondary" to="/list">List</router-link>
      </nav>
    </div>
  <main class="container">
    <router-view :blogData="blogData"></router-view>
  </main>
  </div>
</template>

<script>
import blogData from './assets/blog.js'
export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      blogData
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
