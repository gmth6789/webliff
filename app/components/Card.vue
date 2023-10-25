<template>
  <van-card class="mx-auto" :class="active == true ? 'active': ''" max-width="400">
    <van-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <div class="more-detail" @click="$emit('moreDetail')">More Detail</div>
    </van-img>
    <div class="card-content">
      <div>
        <van-card-text class="text--primary">
          <h1>{{ session.title }}</h1>
        </van-card-text>
        <van-card-subtitle class="pt-0">{{ session.spaker }}</v-card-subtitle>
      </div>
      <van-btn class="circle" @click="$emit('chooseWorkshop')">
        <v-icon>check</v-icon>
      </van-btn>
    </div>
  </van-card>
</template>

<script>
export default {
  props: ['active', 'session']
}
</script>

<style lang="scss" scoped>
.circle {
  height: 32px !important;
  width: 32px !important;
  min-width: auto !important;
  border-radius: 50%;
  color: #fff;
  background: rgba($color: #1a56be, $alpha: 0.3) !important;
  align-self: center;
}
.card-content {
  display: flex;
  justify-content: space-between;
  padding: 15px;
}
.more-detail {
  font-size: 12px;
  color: #1a56be;
  border-radius: 25px;
  padding: 10px 20px;
  background: #fff;
  font-weight: bold;
  display: inline;
  position: absolute;
  bottom: 11px;
  right: 11px;
}
.van-card__subtitle {
  padding: 0;
}
.van-card__text {
  padding: 0;
  padding-bottom: 5px;
  h1 {
    font-size: 24px;
  }
}
.van-card + .v-card {
  margin-top: 30px;
}
.van-card.active {
  .circle {
    background: rgba($color: #1a56be, $alpha: 1) !important;
  }
  .van-image {
    &::before {
      content: "Selected";
      font-weight: bold;
      font-size: 24px;
      height: 100%;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba($color: #1a56be, $alpha: 1) !important;
    }
  }
}
</style>