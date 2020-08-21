<template>
  <div>
      <button @click="reset" type="button" class="button">Reiniciar compra</button>

      <ShoppingCartItems @getValues="setValues" ref="shoppingCartItems"/>
      
      <div class="level has-text-centered">
          <div class="level-item">
              <div>
                  <div class="heading">Total</div>
                    <div class="title">{{amount}}</div>
              </div>
          </div>
          <div class="level-item">
              <div>
                  <div class="heading">Cantidad</div>
                  <div class="title">{{quantity}}</div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import ShoppingCartItems from "./ShopingCartItems";

export default {
  name: "icon",

    props: {},

  data() {
      return {
          amount: 0,
          quantity: 0
      }
  },

    components: {
        ShoppingCartItems
    },

  methods: {
      setValues(obj) {
          this.amount = obj.amount;
          this.quantity = obj.quantity;
      },

      reset() {
          this.$refs.shoppingCartItems.getAll();
      }
  },

  mounted() {
  }
};
</script>

<style>
</style>