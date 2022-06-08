<template>
  <div class="container">
    <app-modal v-if="modalIsOpen" @close="modalToggle"></app-modal>
    <div class="wrapper row">
      <div class="col-xl-2 col-lg-2 col-md-0">
        <div class="left-side">
          <app-navbar></app-navbar>
        </div>
      </div>
      <div class="right-side col-xxl-10 offset-xxl-0 col-xl-9 offset-xl-1 col-lg-9 offset-lg-3 col-md-12">
        <app-body @open="modalToggle" @menuOpen="openMenu"></app-body>
      </div>
    </div>
  </div>
  <app-footer></app-footer>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue'
import AppBody from '@/components/AppBody'
import AppFooter from '@/components/AppFooter'
import AppModal from '@/components/AppModal'

export default {
  name: 'App',
  data () {
    return {
      modalIsOpen: false,
      menuIsOpen: false
    }
  },
  methods: {
    modalToggle () {
      this.modalIsOpen = !this.modalIsOpen
    },
    openMenu () {
      const hamburger = document.querySelector('.main-hamburger')
      const menu = document.querySelector('.left-side')
      let left = 22
      if (window.innerWidth < 568) {
        left = 10
      }
      if (this.menuIsOpen === false) {
        menu.style.left = '0'
        menu.style.width = '230px'
        menu.style.paddingLeft = '15px'
        menu.style.paddingRight = '10px'
        menu.style.zIndex = '9'
        hamburger.style.left = '150px'
        this.menuIsOpen = true
      } else {
        menu.style.left = '-230px'
        hamburger.style.left = left + 'px'
        this.menuIsOpen = false
      }
    }
  },
  components: {
    AppNavbar,
    AppBody,
    AppFooter,
    AppModal
  }
}
</script>

<style lang="sass">
  #app
    height: 100%
    background: -webkit-linear-gradient(90deg, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 50%)
    background: -moz-linear-gradient(90deg, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 50%)
    background: linear-gradient(90deg, rgb(0, 0, 0) 50%, rgb(255, 255, 255) 50%)
    overflow: hidden
  .right-side
    position: relative
    transition: 0.4s all
  .left-side
    position: fixed
    height: 100%
  @media (max-width: 991.98px)
    #app
      background: #fff
    .left-side
      left: -250px
      background-color: #000
      transition: 0.4s all
</style>
