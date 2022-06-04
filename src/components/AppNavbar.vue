<template>
  <div class="navbar">
    <div class="navbar-logo">
      <img src="@/assets/logo.svg" alt="logo">
    </div>
    <ul class="navbar-links">
      <li class="navbar-link">Почему мы</li>
      <li class="navbar-link">Цены</li>
      <li class="navbar-link">Контакты</li>
    </ul>
    <div class="divider"></div>
    <ul class="navbar-services">
      <li class="navbar-services__title">Наши услуги:</li>
      <li class="navbar-service">Разработка сайтов</li>
      <li class="navbar-service">Поддержка сайтов</li>
      <li class="navbar-service">Дизайн сайтов</li>
    </ul>
    <div class="divider"></div>
    <ul class="navbar-contacts">
      <li class="navbar-contact">+7-987-777-67-98</li>
      <li class="navbar-contact">consstudio54@gmail.com</li>
      <li class="navbar-contact">
        <img src="@/assets/icons/wa.svg" alt="WhatsApp">
        WhatsApp
      </li>
      <li class="navbar-contact">
        <img src="@/assets/icons/tg.svg" alt="Telegram">
        Telegram
      </li>
    </ul>
    <div class="navbar-search"></div>
  </div>
</template>

<script>
export default {
  name: 'AppNavbar'
}
</script>

<style scoped lang="sass">
  .navbar
    display: flex
    flex-direction: column
    height: 100%
    ul
      list-style: none
      padding: 0
      color: #ffffff
</style>
