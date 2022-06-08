<template>
  <div class="card d-lg-none d-flex">
    <div class="card-title">{{ item.type }}</div>
    <div class="card-divider"></div>
    <div class="card-desc">{{ item.desc }}</div>
    <div class="card-divider"></div>
    <div class="card-price"><span>Стоимость</span> от {{ item.price }} рублей</div>
    <div class="card-date"><span>Срок</span> от {{ item.deadline }}</div>
    <div class="card-button"><app-button :text="'Заказать сайт'" @open="$emit('open')"></app-button></div>
  </div>
</template>

<script>
import AppButton from '@/components/AppButton'
export default {
  name: 'AppCard',
  emits: ['open'],
  props: ['item'],
  components: { AppButton }
}
</script>

<style scoped lang="sass">
  .card
    display: flex
    flex-direction: column
    width: 290px
    height: 380px
    background-color: #E8E8E9
    box-shadow: 0 4px 5px rgba(0, 0, 0, 0.15)
    border-radius: 10px
    margin-top: 25px
    &-title
      font-size: 19px
      line-height: 30px
      font-family: "Source Sans Pro SemiBold"
      text-transform: uppercase
      margin-top: 20px
    &-desc
      font-size: 18px
      line-height: 28px
      font-family: "Source Sans Pro Regular"
    &-price
      display: flex
      justify-content: space-between
      font-size: 18px
      line-height: 30px
      font-family: "Source Sans Pro Regular"
      margin-bottom: 10px
      span
        font-family: "Source Sans Pro SemiBold"
        font-size: 19px
    &-date
      display: flex
      justify-content: space-between
      font-size: 18px
      line-height: 30px
      font-family: "Source Sans Pro Regular"
      margin-bottom: 30px
      span
        font-family: "Source Sans Pro SemiBold"
        font-size: 19px
    &-button
      text-align: center
    &-divider
      width: 100%
      background-color: rgba(0, 0, 0, 0.4)
      height: 1px
      border-radius: 100%
      margin: 10px 0

@media (max-width: 567.98px)
    .card
      height: 350px
      &-title
        font-size: 17px
      &-desc
        font-size: 16px
      &-price
        font-size: 17px
        span
          font-size: 17px
      &-date
        font-size: 17px
        span
          font-size: 17px
</style>
