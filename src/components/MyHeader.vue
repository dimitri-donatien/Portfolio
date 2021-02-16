<template>
  <div>
    <my-menu></my-menu>
    <my-social></my-social>
  </div>
</template>

<script>
// @ is an alias to /src
import MyMenu from './MyMenu'
import MySocial from './MySocial'

export default {
  name: 'MyHeader',
  components: {
    MyMenu,
    MySocial
  },
}
</script>

<style lang="scss" scoped>

</style>