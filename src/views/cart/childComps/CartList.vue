<template>
  <div class="cart-list">
    <cart-list-item
      v-for="(item, index) in cartList"
      :key="index"
      :product="item"
    />
  </div>
</template>

<script>
import CartListItem from "./CartListItem";

import { mapGetters } from "vuex";

export default {
  name: "CartList",
  components: {
    CartListItem
  },
  computed: {
    ...mapGetters(["cartList"])
  }
};
</script>

<style>
.cart-list {
  height: calc(100% - 44px - 49px);
}

.content {
  height: 100%;
  overflow: hidden;
}
</style>
