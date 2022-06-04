<template>
 <div class="footer">
   <div class="container">
     <ul>
       <li>Наш официальный сайт: https://www.consstudio.ru</li>
       <li>Copyright c 2021- 2022</li>
       <li>Политика конфиденциальности</li>
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
      height: 100%
      display: flex
      justify-content: space-between
      color: #ffffff
      list-style: none
      padding: 0
      margin: 0
      align-items: center
</style>
