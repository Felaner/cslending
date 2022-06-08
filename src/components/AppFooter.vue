<template>
 <div class="footer">
   <div class="container">
     <ul>
       <li><a class="footer-link" href="https://consstudio.ru/" target="_blank">Наш официальный сайт: https://www.consstudio.ru</a></li>
       <li>Copyright c 2021- 2022</li>
       <li><a class="footer-link" href="https://consstudio.ru/policy" target="_blank">Политика конфиденциальности</a></li>
     </ul>
   </div>
 </div>
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style scoped lang="sass">
  .footer
    height: 120px
    background: #050321
    .container
      height: 100%
    ul
      position: relative
      height: 100%
      display: flex
      justify-content: space-between
      color: rgba(255, 255, 255, 0.6)
      list-style: none
      padding: 0
      margin: 0
      align-items: center
      font-size: 16px
      line-height: 28px
      font-family: "Source Sans Pro Light"
      li
        &:nth-child(2)
          position: absolute
          left: 50%
          transform: translateX(-50%)
    &-link
      color: rgba(255, 255, 255, 0.6)
      text-decoration: none
      &:hover
        color: #fefefe
        text-decoration: none
  @media (max-width: 991.98px)
    .footer
      ul
        flex-direction: column
        justify-content: space-around
        li
          &:nth-child(2)
            position: inherit
            left: unset
            transform: unset
  @media (max-width: 567.98px)
    .footer
      ul
        li
          text-align: center
</style>
