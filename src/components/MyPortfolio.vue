<template>
  <section class="portfolio-content">
    <h2 class="font-bold text-white text-3xl mb-8 md:mb-0 md:text-4xl">Portfolio<span class="text-red-600">_</span></h2>
    <div class="content-card">
      <my-card :image="require('@/assets/img/227944.jpg')"></my-card>
      <my-card :image="require('@/assets/img/227944.jpg')"></my-card>
      <my-card :image="require('@/assets/img/227944.jpg')"></my-card>
      <my-card :image="require('@/assets/img/227944.jpg')"></my-card>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import MyCard from './MyCard'

export default {
  name: 'MyPortfolio',
  components: {
    MyCard
  }

}
</script>

<style lang="scss" scoped>
  .portfolio-content {
    min-height: 100vh;
    width: 100%;
    background: #121212;
    padding: 1rem;
  }
  .content-card {
    display: grid;
    grid-template-columns: repeat( auto-fit, minmax(250px, 1fr));
    place-items: center;
    min-height: 100vh;
    gap: 1rem;
  }
</style>