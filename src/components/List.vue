<template>
  <div class="row mb-2">
    <div class="" v-for="data in blogData" :key=data.number>
      <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
        <div class="col p-4 d-flex flex-column position-static">
          <h3 class="mb-0">{{data.title}}</h3>
          <div class="mb-1 text-muted">{{data.date}}</div>
          <p class="card-text mb-auto">{{data.content}}</p>
          <!-- <router-link class="stretched-link" :to="'/detail/' + data.number">Continue reading</router-link> -->
          <a class="stretched-link" @click="$router.push('/detail/' + data.number)">Continue reading</a>
        </div>
      </div>
    </div>
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