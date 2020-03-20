<template>
  <el-container>
    <el-aside>
      SideMenu
    </el-aside>
    <el-container>
      <el-header>
        Top Search Bar
      </el-header>
      <el-main>
        <offer-page />
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
import OfferPage from './components/OffersPage.vue'

export default {
  name: 'App',
  components: {
    OfferPage
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
