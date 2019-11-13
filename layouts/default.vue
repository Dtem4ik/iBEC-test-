<template>
  <div class="main">
    <Header />
    <Nav />
    <nuxt />
  </div>
</template>
<script>
import Header from '@/components/Header'
import Nav from '@/components/Nav'
export default {
  components: {
    Header,
    Nav
  }
}
</script>
<style lang="scss">
body{
  background: #e3e3e3;
}
.main{
  min-height: 100vh;
  width: 100%;
  background:
    url(/img/Layer7.png) no-repeat,
    url(/img/Layer6.png) no-repeat
}
</style>
