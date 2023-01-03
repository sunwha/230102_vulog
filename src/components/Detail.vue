<template>
  <div class="row g-5">
    <h3 class="pb-4 mb-4 fst-italic border-bottom">Details...</h3>
    <article class="blog-post">
        <h2 class="blog-post-title mb-1">{{blogData[$route.params.id].title}}</h2>
        <p class="blog-post-meta">{{blogData[$route.params.id].date}}</p>
        <p>{{blogData[$route.params.id].content}}</p>
        <router-view></router-view>
    </article>
  </div>
</template>

<script>
export default {
    props: {
        blogData: Array
    }
}
</script>

<style>

</style>