<template>
  <form class="modal" id="modal">
    <div class="modal-title">
      Заявка на создание сайта
    </div>
    <div class="modal-name">
      <label for="name">Ваше ФИО<input type="text" id="name" placeholder="ФИО"></label>
    </div>
    <div class="modal-phone">
      <label for="phone">Ваш номер телефона<input type="number" id="phone" placeholder="Телефон"></label>
    </div>
    <div class="modal-mail">
      <label for="mail">Ваш Email<input type="text" id="mail" placeholder="Email"></label>
    </div>
    <div class="modal-info">
      <label for="info">Дополнительная информация<textarea name="info" id="info"></textarea></label>
    </div>
    <button class="modal-close" @click="$emit('close')"><img src="@/assets/icons/close.svg" alt="close"></button>
    <div class="modal-send">
      <button>Отправить</button>
    </div>
  </form>
</template>

<script>
export default {
  name: 'AppModal',
  emits: ['close']
}
</script>

<style scoped lang="sass">
  .modal
    display: block
    position: fixed
    top: 50%
    left: 50%
    transform: translate(-50%, -50%)
    height: auto
    width: 600px
    background-color: #1b1f27
    z-index: 10
    padding: 40px 0
    z-index: 15
    &-title
      text-align: center
      color: #fff
      font-size: 22px
      font-family: "Source Sans Pro SemiBold"
    &-name
      margin-top: 20px
      padding: 0 60px
      label
        display: flex
        flex-direction: column
        color: #fff
        font-family: "Source Sans Pro SemiBold"
        input
          margin-top: 10px
          height: 40px
          width: 100%
          padding-left: 10px
    &-phone
      margin-top: 20px
      padding: 0 60px
      label
        display: flex
        flex-direction: column
        color: #fff
        font-family: "Source Sans Pro SemiBold"
        input
          margin-top: 10px
          height: 40px
          width: 100%
          padding-left: 10px
        input[type="number"]::-webkit-outer-spin-button,
        input[type="number"]::-webkit-inner-spin-button
          -webkit-appearance: none
        input[type='number'],
        input[type="number"]:hover,
        input[type="number"]:focus
          appearance: none
          -moz-appearance: textfield
    &-mail
      margin-top: 20px
      padding: 0 60px
      label
        display: flex
        flex-direction: column
        color: #fff
        font-family: "Source Sans Pro SemiBold"
        input
          margin-top: 10px
          height: 40px
          width: 100%
          padding-left: 10px
    &-info
      margin-top: 20px
      padding: 0 60px
      label
        display: flex
        flex-direction: column
        color: #fff
        font-family: "Source Sans Pro SemiBold"
        textarea
          margin-top: 10px
          height: 90px
          width: 100%
          padding-left: 10px
        textarea:active, textarea:hover, textarea:focus
          outline: 0
          outline-offset: 0
    &-close
      position: absolute
      right: 0
      top: 0
      width: 50px
      height: 50px
      background: none
      border: none
      cursor: pointer
      img
        width: 100%
    &-send
      display: flex
      justify-content: center
      button
        background-color: #25045C
        box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.15)
        border: none
        border-radius: 5px
        padding: 16px 51px
        color: #FEFEFE
        font-size: 18px
        text-align: center
        text-transform: uppercase
        letter-spacing: 2px
        margin-top: 20px
        font-family: "Bebas Neue Regular"
        cursor: pointer
  @media (max-width: 1399.98px)
    .modal
      &-send
        button
          padding: 11px 28px
          font-size: 16px
  @media (max-width: 1199.98px)
    .modal
      &-send
        button
          padding: 10px 20px
          font-size: 15px
  @media (max-width: 767.98px)
    .modal
      width: 90%
      height: auto
      &-name
        padding: 0 15px
      &-phone
        padding: 0 15px
      &-mail
        padding: 0 15px
      &-info
        padding: 0 15px
</style>
