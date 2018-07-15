<template lang="pug">
  #app
    .step-bar
      .step-point.now
      .step-point
      .step-point
      .step-point
    .title
      h1 Create Account
      h2 Glad to see you here!
    .form-wrap
      .form-item
        label(for="") Account
        input(type="text" placeholder="example@email.com")
      .form-item
        label(for="") Password
        input(type="password")
      .form-item
        label(for="") Comfirm Password
        input(type="password")
      button.btn SUBMIT & NEXT

</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="sass">
@import './assets/style/main.sass'
#app
  max-width: 460px
  width: 100%
  height: auto
  border-top: 3px solid $color_primary
  display: flex
  align-items: center
  flex-direction: column
  .step-bar
    position: relative
    width: 55%
    height: 16px
    display: flex
    justify-content: space-between
    margin-top: 60px
    &:before
      content: ''
      border-top: 2px solid $color_second
      width: 100%
      position: absolute
      top: 50%
      z-index: -1
    .step-point
      width: 16px
      height: 16px
      border: 2px solid $color_second
      border-radius: 50%
      background-color: white
      z-index: 2
      display: flex
      justify-content: center
      align-items: center
      &.now
        border-color: $color_primary
        &:after
          content: ''
          display: inline-block
          width: 8px
          height: 8px
          background-color: $color_primary
          border-radius: 50%
  .title
    width: 100%
    margin-top: 40px
    h1,h2
      text-align: center
  .form-wrap
    margin-top: 25px
    width: 100%
    >.form-item:not(:last-child)
      margin-bottom: 24px
    .form-item
      label
        display: inline-block
        margin-bottom: 8px
      input
        width: 100%
        height: 52px
        border: 2px solid #000
        border-radius: 8px
        padding-left: 14px
        font-size: 20px
  .btn
    background-color: $color_second
    color: white
    border: none
    outline: none
    width: 100%
    height: 52px
    border-radius: 8px
    cursor: not-allowed
    font-size: 20px

</style>
