<template>
  <button class="main-hamburger d-lg-none d-flex" @click="$emit('open')">
    <span></span>
    <span></span>
  </button>
  <div class="main">
    <img class="main-bg" src="@/assets/images/main-bg.jpg" alt="img">
    <div class="main-button__top">
      <app-button :text="'Заказать сайт'" @open="$emit('open')"></app-button>
    </div>
    <h1 class="title">Студия веб-разработки <br>Consequat</h1>
    <p class="subtitle">Наша организация специфицируется на создании сайтов. Мы создадим <br>для вас уникальный проект с нуля или же доработаем действующий.</p>
    <button class="universal__button-circle position-absolute scroll-to__order" @click="$emit('open')">
      <span class="universal__button-circle-text">Оставить заявку</span>
      <div class="universal__button-circle-wrapper">
        <div class="universal__button-circle-arrow"></div>
        <div class="universal__button-circle-border"></div>
        <div class="universal__button-circle-mask">
          <div class="universal__button-circle-small"></div>
        </div>
      </div>
    </button>
  </div>
  <div class="about" id="about">
    <h2 >Почему мы?</h2>
    <ul class="about-list">
      <li class="about-item">
        Лояльные цены на услуги web-разработки.
      </li>
      <li class="about-item">
        Приверженность качеству исполнения каждого проекта. В своей работе мы ценим ресурсы клиентов и стараемся находить индивидуальный подход к самой уникальной задаче.
      </li>
      <li class="about-item">
        Работа как с техническим заданием, так и с нашими предложениями по наилучшей реализации ваших идей.
      </li>
      <li class="about-item">
        Анализ ваших конкурентов перед началом разработки сайта, что бы добиться наиболее качественного продукта.
      </li>
      <li class="about-item">
        Гарантия уникальности. Уделяем особое внимание оформлению и дизайну сайта, добавляя акцент на идею бренда.
      </li>
      <li class="about-item">
        Высокая скорость загрузки сайта и качество пользования ресурсом.
      </li>
      <li class="about-item">
        Подберем узнаваемый и запоминающийся домен, который будет отражать идею вашего бренда. Настроим оптимальную работу хостинга.
      </li>
      <li class="about-item">
        Оперативное внесение незначительных правок после запуска вашего сайта.
      </li>
      <li class="about-item">
        Техническая поддержка. Бесплатное консультирование по вопросам ведения сайта в первый месяц после сдачи проекта.
      </li>
    </ul>
  </div>
  <div class="price" id="price">
    <h2>Цены на создание сайтов</h2>
    <ul class="price-list__column d-lg-flex d-none">
      <li>Название</li>
      <li>Описание</li>
      <li>Стоимость</li>
      <li>Срок</li>
    </ul>
    <div class="divider"></div>
    <div class="row cards-wrapper d-lg-none">
      <app-card v-for="(item, index) of sites" :key="index" :item="item" @open="$emit('open')"></app-card>
    </div>
    <div class="price-list d-lg-block d-none" v-for="item of sites" :key="item.type">
      <ul>
        <li>{{ item.type }}</li>
        <li>{{ item.desc }}</li>
        <li>От {{ item.price }} рублей</li>
        <li>{{ item.deadline }}</li>
        <li><app-button :text="'Заказать сайт'" @open="$emit('open')"></app-button></li>
      </ul>
      <div class="divider"></div>
    </div>
  </div>
  <div class="price-mobile">

  </div>
  <div class="contacts" id="contacts">
    <h2>Контакты</h2>
    <ul>
      <li><span>Адрес: </span> г.Новосибирск</li>
      <li><a href=""><span>Телефон: </span> +7-987-777-67-98</a></li>
      <li><a href=""><span>E-mail: </span> consstudio54@gmail.com</a></li>
      <li>
        <a href="">
          <img src="@/assets/icons/wa.svg" alt="WhatsApp">
          WhatsApp
        </a>
      </li>
      <li>
        <a href="">
          <img src="@/assets/icons/tg.svg" alt="Telegram">
          Telegram
        </a>
      </li>
    </ul>
    <div class="divider"></div>
    <div class="map">
      <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3Aaa6d300e540917c4062a675634c1828814b161b4fc9c69b407ecb6c3a07cca20&amp;source=constructor" width="100%" height="435" frameborder="0"></iframe>
    </div>
  </div>
</template>

<script>
import AppButton from '@/components/AppButton'
import AppCard from '@/components/AppCard'
export default {
  name: 'AppBody',
  emits: ['menuOpen', 'open'],
  data () {
    return {
      sites: [
        {
          type: 'Landing-page',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Сайт-визитка',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Корпоративный сайт',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Блог',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Интернет-каталог',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Дизайн',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Адаптивный дизайн',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        },
        {
          type: 'Редизайн сайта',
          desc: 'Веб-страница, основной задачей которой является сбор контактных данных целевой аудитории.',
          price: '20000',
          deadline: 'от 1 месяца'
        }
      ],
      mainHeight: 0
    }
  },
  mounted () {
    const hamburger = document.querySelector('.main-hamburger')
    this.mainHeight = document.querySelector('.main-bg').clientHeight - hamburger.style.top - 30
    window.addEventListener('scroll', () => {
      const hamLines = hamburger.querySelectorAll('span')
      hamLines.forEach(el => {
        if (window.top.scrollY > this.mainHeight) {
          el.style.backgroundColor = '#000000'
        } else {
          el.style.backgroundColor = '#ffffff'
        }
      })
    })
  },
  components: { AppCard, AppButton }
}
</script>

<style scoped lang="sass">
  .main
    position: relative
    padding: 240px 0 210px 70px
    &-bg
      position: absolute
      top: 0
      left: 0
      object-fit: cover
      width: 100vw
      height: 100%
    &-button
      &__top
        position: absolute
        top: 40px
        right: 0
    .title
      position: relative
      font-size: 44px
      font-family: "Bebas Neue Bold"
      letter-spacing: 10px
      line-height: 58px
      color: #fefefe
      z-index: 1
    .subtitle
      position: relative
      font-size: 18px
      font-family: "Source Sans Pro SemiBold"
      line-height: 28px
      margin-bottom: 90px
      color: #fefefe
      z-index: 1
    .universal
      &__button-circle
        $this: &
        display: flex
        cursor: pointer
        align-items: center
        padding-right: 65px
        height: 80px
        background: none
        border: none
        &-text
          z-index: 1
          font-size: 16px
          margin-right: 20px
          margin-bottom: 4px
          color: #fefefe
        &-wrapper
          position: relative
          display: flex
          align-items: center
        &-arrow
          display: flex
          position: absolute
          align-items: center
          left: 12px
          height: 3px
          width: 75px
          background-color: #fefefe
          &:after
            content: ""
            width: 0
            height: 0
            top: -5px
            right: -7px
            position: absolute
            border-top: 7px solid transparent
            border-bottom: 7px solid transparent
            border-left: 7px solid #fefefe
        &-border
          width: 50px
          height: 50px
          border-radius: 50%
          border: 1px solid #fefefe
          transition: transform 987ms
        &-mask
          width: 50px
          height: 50px
          position: absolute
          border-radius: 50%
          display: flex
          align-items: center
          justify-content: center
          clip-path: circle(25px)
          transition: -webkit-clip-path 987ms
          transition: clip-path 987ms
        &-small
          width: 16px
          height: 16px
          border-radius: 50%
          transform: translateX(63px)
          background-color: #fefefe
        &:hover
          .universal__button-circle-border
            transform: translateX(63px)
          .universal__button-circle-mask
            clip-path: circle(25px at 85px)
  .about
    padding: 70px 30px
    background: #ffffff
    h2
      color: #000000
      font-size: 20px
      font-family: "Source Sans Pro Bold"
      line-height: 25px
      text-transform: uppercase
    &-list
      color: #000000
      font-size: 18px
      line-height: 28px
      font-family: "Source Sans Pro Regular"
  .price
    padding: 0 0 70px 30px
    background: #ffffff
    h2
      margin: 0
      color: #000000
      font-size: 20px
      font-family: "Source Sans Pro Bold"
      line-height: 25px
      text-transform: uppercase
    &-list
      ul
        display: flex
        align-items: center
        position: relative
        list-style: none
        padding: 0
        li
          &:first-child
            font-size: 19px
            line-height: 30px
            font-family: "Source Sans Pro SemiBold"
            width: 234px
          &:nth-child(2)
            font-size: 18px
            line-height: 28px
            font-family: "Source Sans Pro Regular"
            width: 308px
          &:nth-child(3)
            font-size: 19px
            line-height: 30px
            font-family: "Source Sans Pro SemiBold"
            width: 117px
          &:nth-child(4)
            font-size: 19px
            line-height: 30px
            font-family: "Source Sans Pro SemiBold"
            width: 120px
          &:last-child
            position: absolute
            right: 0
            width: 236px
            text-align: end
      &__column
        list-style: none
        margin-top: 30px
        padding: 0
        li
          font-size: 19px
          line-height: 30px
          font-family: "Source Sans Pro SemiBold"
          &:first-child
            width: 234px
          &:nth-child(2)
            width: 308px
          &:nth-child(3)
            width: 117px
          &:last-child
            width: 236px
  .contacts
    background: #ffffff
    padding: 0 30px
    h2
      margin-top: 0
      margin-bottom: 30px
      color: #000000
      font-size: 20px
      font-family: "Source Sans Pro Bold"
      line-height: 25px
      text-transform: uppercase
    ul
      display: flex
      justify-content: space-between
      align-items: center
      list-style: none
      margin: 0
      margin-bottom: 20px
      padding: 0
      li
        font-size: 19px
        line-height: 30px
        font-family: "Source Sans Pro Regular"
        span
          font-family: "Source Sans Pro SemiBold"
        a
          display: flex
          align-items: center
          color: #000
          text-decoration: none
          &:hover
            color: #000
            text-decoration: none
          span
            font-family: "Source Sans Pro SemiBold"
            margin-right: 8px
        &:nth-child(4)
          display: flex
          align-items: center
          img
            margin-right: 10px
        &:nth-child(5)
          display: flex
          align-items: center
          img
            margin-right: 10px
    .map
      height: 505px
      width: 100%
  @media (max-width: 1399.98px)
    .main
      padding: 190px 0 190px 70px
    .price
      padding: 0 0 30px 30px
      &-list__column
        li
          &:first-child
            width: 154px
          &:nth-child(2)
            font-size: 16px
            width: 255px
            margin-right: 10px
          &:nth-child(3)
            font-size: 17px
          &:nth-child(4)
            font-size: 17px
      &-list
        ul
          li
            &:first-child
              width: 154px
            &:nth-child(2)
              font-size: 16px
              width: 255px
              margin-right: 10px
            &:nth-child(3)
              font-size: 17px
            &:nth-child(4)
              font-size: 17px
    .contacts
      h2
        margin-bottom: 15px
      ul
        flex-direction: column
        align-items: start
        li
          &:nth-child(4)
            margin: 8px 0
  @media (max-width: 1199.98px)
    .price
      &-list__column
        li
          &:nth-child(2)
            width: 150px
          &:nth-child(3)
            width: 110px
          &:nth-child(4)
            width: 81px
      &-list
        ul
          li
            &:nth-child(2)
              width: 150px
            &:nth-child(3)
              width: 110px
            &:nth-child(4)
              width: 81px
  @media (max-width: 991.98px)
    .main
      padding: 190px 0 190px 0
      &-bg
        left: -148px
        width: auto
    .price
      padding: 0 0 30px 0
      .cards-wrapper
        display: flex
        justify-content: space-around
    .about
      padding: 70px 0
    .contacts
      padding: 0
    .main-hamburger
      display: flex
      flex-direction: column
      justify-content: space-between
      position: fixed
      width: 50px
      height: 30px
      padding: 9px
      left: 22px
      top: 43px
      background: none
      border: none
      cursor: pointer
      z-index: 10
      transition: 0.4s all
      span
        width: 100%
        height: 2px
        background-color: #fff
  @media (max-width: 767.98px)
    .main
      padding: 150px 0 150px 0
      .subtitle
        margin-bottom: 50px
  @media (max-width: 567.98px)
    .main
      padding: 130px 0 120px 0
      .title
        font-size: 26px
        text-align: center
        letter-spacing: 5px
        line-height: 40px
      .subtitle
        text-align: center
      .universal__button-circle
        position: absolute
        left: 50%
        transform: translateX(-50%)
    .about
      padding: 40px 0
      h2
        font-size: 18px
      &-list
        font-size: 16px
    .main-hamburger
      left: 10px
      top: 20px
    .price
      h2
        font-size: 18px
    .contacts
      h2
        font-size: 18px
      ul
        li
          font-size: 16px
      .map
        height: 320px
        iframe
          height: 80%
</style>
