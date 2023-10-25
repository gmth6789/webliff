<template>
  <van-app>
    <nuxt></nuxt>
    <Dialog/>
  </van-app>
</template>

<script>
import Dialog from '~/components/Dialog'

export default {
  components: {
    Dialog
  }
}
</script>

<style lang="scss">
  .van-application{
    font-family: 'Quicksand', sans-serif;
  }
  .van-toolbar__title{
    text-align: center;
    width: 100%;
    font-weight: bold;
  }
  .van-application .primary{
    background-color: #1A56BE !important;
    border-color: #1A56BE !important;
  }
  .text-primary{
    color: #1A56BE !important;
  }
  .bold{
    font-weight: bold;
  }
  .text-main{
    font-size: 20px;
  }
  .text-title{
    font-size: 20px;
    font-weight: bold;
  }
  .w-100{
    width: 100%;
  }
  .my-btn{
    font-size: 20px !important;
    text-transform: none !important;
    height: auto !important;
    padding: 10px 0 !important;
    font-weight: bold;
    min-height: 50px;
    &.outlined{
      border: 1px solid #1A56BE;
      border-radius: 28px;
      line-height: normal;
    }
  }
  .mt-100{
    margin-top: 100px;
  }
  .set-padding{
    padding: 0 10px;
  }
</style>