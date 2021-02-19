<template>
  <section id="portfolio" class="portfolio-content">
    <h2 class="font-bold text-white text-3xl mb-8 md:mb-4 md:text-4xl">Portfolio<span class="text-red-600">_</span></h2>
    <div class="item-grid">
      <my-card :image="require('@/assets/img/Landing.jpg')" category="Ui/UX" title="Love It"></my-card>
      <my-card :image="require('@/assets/img/Landing-Blog.jpg')" category="Ui/UX" title="Landing Page Blog"></my-card>
      <my-card :image="require('@/assets/img/Food-Design.jpg')" category="Ui/UX" title="Food Fitness"></my-card>
      <my-card :image="require('@/assets/img/Sing-in-anime.jpg')" category="Ui/UX" title="Anime website sing in"></my-card>
      <my-card :image="require('@/assets/img/Landing-Page-Hosting.jpg')" category="Ui/UX" title="Landing Hosting"></my-card>
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

  .item-grid {
    display: grid;
    grid-template-columns: repeat( auto-fit, minmax(325px, 1fr));
    gap: 1rem;
  }
</style>