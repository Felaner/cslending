<template>
  <button @click="$emit('open')">{{ text }}</button>
</template>

<script>
export default {
  name: 'AppButton',
  emits: ['open'],
  props: ['text']
}
</script>

<style scoped lang="sass">
  button
    background-color: #25045C
    box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.15)
    border: none
    border-radius: 5px
    padding: 16px 51px
    color: #FEFEFE
    font-size: 18px
    text-transform: uppercase
    letter-spacing: 2px
    font-family: "Bebas Neue Regular"
    cursor: pointer
  @media (max-width: 1399.98px)
    button
      padding: 11px 28px
      font-size: 16px
  @media (max-width: 1199.98px)
    button
      padding: 10px 20px
      font-size: 15px
</style>
