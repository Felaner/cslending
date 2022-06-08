<template>
  <div class="navbar">
    <div class="navbar-logo">
      <img src="@/assets/logo.svg" alt="logo">
    </div>
    <ul class="navbar-links">
      <li class="navbar-link"><a href="">Почему мы</a></li>
      <li class="navbar-link"><a href="">Цены</a></li>
      <li class="navbar-link"><a href="">Контакты</a></li>
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
      <li class="navbar-contact"><a class="navbar-contact__link" href="tel:+79877776798">+7-987-777-67-98</a></li>
      <li class="navbar-contact"><a class="navbar-contact__link" href="mailto:consstudio54@gmail.com">consstudio54@gmail.com</a></li>
      <li class="navbar-contact">
        <a class="navbar-contact__link" href="">
          <img src="@/assets/icons/wa.svg" alt="WhatsApp">
          WhatsApp
        </a>
      </li>
      <li class="navbar-contact">
        <a class="navbar-contact__link" href="">
          <img src="@/assets/icons/tg.svg" alt="Telegram">
          Telegram
        </a>
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
    justify-content: center
    height: 100%
    ul
      list-style: none
      padding: 0
      color: #ffffff
    &-links
      margin-top: 70px
      font-size: 20px
      line-height: 25px
      text-transform: uppercase
      font-family: "Source Sans Pro Regular"
      .navbar-link
        margin-bottom: 8px
        a
          color: #fefefe
          text-decoration: none
        &:last-child
          margin-bottom: 0
    .divider
      width: 100%
      height: 1px
      background-color: rgba(254, 254, 254, 0.4)
      border-radius: 100%
      margin: 25px 0
    &-services
      margin-top: 15px
      font-size: 20px
      line-height: 25px
      text-transform: uppercase
      font-family: "Source Sans Pro Bold"
      &__title
        margin-bottom: 9px
      .navbar-service
        margin-bottom: 9px
        font-family: "Source Sans Pro Regular"
        &:last-child
          margin-bottom: 0
    &-contacts
      font-size: 20px
      line-height: 25px
      .navbar-contact
        font-family: "Source Sans Pro Regular"
        color: rgba(254, 254, 254, 0.7)
        margin-bottom: 9px
        &__link
          text-decoration: none
        &:first-child
          a
            color: #fefefe
        &:nth-child(2)
          a
            color: rgba(254, 254, 254, 0.7)
            &:hover
              color: #fefefe
              text-decoration: none
        &:nth-child(3)
          a
            display: flex
            align-items: center
            color: rgba(254, 254, 254, 0.7)
            &:hover
              color: #fefefe
              text-decoration: none
            img
              margin-right: 10px
        &:nth-child(4)
          a
            display: flex
            align-items: center
            color: rgba(254, 254, 254, 0.7)
            margin-bottom: 0
            &:hover
              color: #fefefe
              text-decoration: none
            img
              margin-right: 10px
  @media (max-width: 1399.98px)
    .navbar
      &-links
        margin-top: 40px
        margin-bottom: 0
        font-size: 18px
      .divider
        margin: 15px 0
      &-services
        margin-top: 0
        margin-bottom: 0
        font-size: 18px
      &-contacts
        margin-top: 0
        font-size: 18px
</style>
