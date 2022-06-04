<template>
  <div class="main">
    <button>Заказать сайт</button>
    <h1 class="title">Студия веб-разработки <br>Consequat</h1>
    <p class="subtitle">Наша организация специфицируется на создании сайтов. Мы создадим <br>для вас уникальный проект с нуля или же доработаем действующий.</p>
    <button>Оставить заявку</button>
  </div>
  <div class="about">
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
  <div class="price">
    <h2>Цены на создание сайтов</h2>
    <ul class="price-list__column">
      <li>Название</li>
      <li>Описание</li>
      <li>Стоимость</li>
      <li>Срок</li>
    </ul>
    <div class="divider"></div>
    <div class="price-list" v-for="item of sites" :key="item.type">
      <ul>
        <li>{{ item.type }}</li>
        <li>{{ item.desc }}</li>
        <li>От {{ item.price }} рублей</li>
        <li>{{ item.deadline }}</li>
        <li><button>Заказать сайт</button></li>
      </ul>
      <div class="divider"></div>
    </div>
  </div>
  <div class="contacts">
    <ul>
      <li>Адрес: г.Новосибирск</li>
      <li>Телефон: +7-987-777-67-98</li>
      <li>E-mail: consstudio54@gmail.com</li>
      <li>
        <img src="@/assets/icons/wa.svg" alt="WhatsApp">
        WhatsApp
      </li>
      <li>
        <img src="@/assets/icons/tg.svg" alt="Telegram">
        Telegram
      </li>
    </ul>
    <div class="divider"></div>
    <div class="map"></div>
  </div>
</template>

<script>
export default {
  name: 'AppBody',
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
      ]
    }
  }
}
</script>

<style scoped lang="sass">
  .main
    position: relative
    padding: 240px 0 210px 70px
    background: #ffffff
    button
      &:first-child
        position: absolute
        top: 40px
        right: 0
  .about
    padding: 70px 30px
    background: #ffffff
    h2
      color: #000000
    &-list
      color: #000000
  .price
    padding: 0 30px 70px
    background: #ffffff
    h2
      margin: 0
    &-list
      ul
        display: flex
        list-style: none
        padding: 0
        li
          &:first-child
            width: 234px
          &:nth-child(2)
            width: 308px
          &:nth-child(3)
            width: 117px
          &:last-child
            width: 236px
      &__column
        display: flex
        list-style: none
        margin-top: 30px
        padding: 0
        li
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
    ul
      display: flex
      justify-content: space-between
      list-style: none
      margin: 0
      padding: 0
    .map
      height: 435px
      width: 100%
      background: #000
</style>
