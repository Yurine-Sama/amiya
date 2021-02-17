<template>
  <div>

  </div>
</template>
<script>
export default {
  // name: "Hello World",
  props: {
    image: String,
    title: String,
    price: Number
  },
  data() {
    return {
      buy: 0
    };
  },
  methods: {
    BuyClink() {
      this.buy++, this.$emit("callbackBuy", this.buy);
    },

    CancelClink() {
      this.cancel--, this.$emit("callbackCancel", this.cancel);
    }
  }
};
</script>
