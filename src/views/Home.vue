<template>
  <div class="home">
    <my-header></my-header>
    <my-portfolio></my-portfolio>
    <my-about></my-about>
    <my-capabilities></my-capabilities>
    <my-footer></my-footer>
  </div>
</template>

<script>
// @ is an alias to /src
import MyHeader from '@/components/MyHeader'
import MyPortfolio from '@/components/MyPortfolio'
import MyAbout from '@/components/MyAbout'
import MyCapabilities from '@/components/MyCapabilities'
import MyFooter from '@/components/MyFooter'

export default {
  name: 'Home',
  components: {
    MyHeader,
    MyPortfolio,
    MyAbout,
    MyCapabilities,
    MyFooter
  },
}
</script>

<style lang="scss" scoped>

</style>