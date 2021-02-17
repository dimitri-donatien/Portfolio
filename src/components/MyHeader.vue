<template>
  <header class="background-header min-h-screen w-full grid grid-cols-1 md:grid-cols-2 text-white p-4">
    <!-- <my-logo></my-logo> -->
    <!-- <my-menu></my-menu> -->
    <section class="flex place-items-center">
      <img class="w-full h-auto" :src="require('@/assets/svg/pixeltrue-web-development.svg')" alt="">
    </section>
    <section class="flex flex-col md:justify-center">
      <div class="flex flex-col mb-6">
        <h1 class="font-bold text-3xl lg:text-4xl">Dimitri Donatien</h1>
        <h2 class="font-semibold text-2xl lg:text-3xl">Concepteur développeur d'applications</h2>
      </div>
      <div class="flex lg:text-2x1">
        <p class="mr-2">UI-UX Design</p>
        <span class="text-red-400">/</span>
        <p class="mr-2 ml-2">Web Dev</p>
        <span class="text-red-400">/</span>
        <p class="mr-2 ml-2">Mobile Dev</p>
      </div>
    </section>
  </header>
</template>

<script>
// @ is an alias to /src
// import MyMenu from './MyLogo'
// import MyMenu from './MyMenu'

export default {
  name: 'MyHeader',
  components: {
    // MyLogo,
    // MyMenu,
  },
}
</script>

<style lang="scss" scoped>

.background-header {
  background-color: #131313;
}

</style>