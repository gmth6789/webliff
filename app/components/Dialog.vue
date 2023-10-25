<template>
  <van-dialog
    v-model="getDialog.isShow"
    max-width="290"
    persistent
  >
    <van-card>
      <van-card-title>{{ getDialog.title }}</van-card-title>
      <van-card-text v-html="getDialog.message"></van-card-text>
      <van-card-actions>
          <van-spacer></van-spacer>
          <van-btn
            color="green darken-1"
            text
            @click="hideDialog"
          >
            Close
          </van-btn>
        </van-card-actions>
    </v-card>
  </van-dialog>
</template>

<script>
export default {
  computed: {
    getDialog(){
      return this.$store.getters.getDialog
    }
  },
  methods: {
    hideDialog(){
      this.$store.dispatch('setDialog', {
        isShow: false,
        title: '',
        message: ''
      })
    }
  } 
}
</script>