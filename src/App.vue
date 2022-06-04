<template>
  <div class="container">
    <div class="wrapper row">
      <div class="col-xl-2">
        <div class="left-side">
          <app-navbar></app-navbar>
        </div>
      </div>
      <div class="right-side col-xl-10">
        <app-body></app-body>
      </div>
    </div>
  </div>
  <app-footer></app-footer>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue'
import AppBody from '@/components/AppBody'
import AppFooter from '@/components/AppFooter'

export default {
  name: 'App',
  components: {
    AppNavbar,
    AppBody,
    AppFooter
  }
}
</script>

<style lang="sass">
  #app
    height: 100%
    background: -webkit-linear-gradient(90deg, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 50%)
    background: -moz-linear-gradient(90deg, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 50%)
    background: linear-gradient(90deg, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 50%)
  .left-side
    position: fixed
    height: 100%
</style>
