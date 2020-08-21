<template>
  <table class="table is-fullwidth">
      <tbody>
            <tr v-for="(item, index) in items" :key="index">
                <td>{{item.name}}</td>
                <td style="width: 100px;" class="has-text-right">$ {{item.price.toFixed(2)}}</td>
                <td style="width: 100px;" class="has-text-right">
                <button @click="remove(index)" class="button is-danger">Retirar</button>
                </td>
            </tr>
      </tbody>
  </table>
</template>

<script>
export default {
  name: "ShoppinCartItems",

    props: {},

  data() {
      return {
          items: []
      }
  },

  methods: {
      getAll() {
          this.items = [
              { name: "Producto A", price: 25},
              { name: "Producto B", price: 37.2},
              { name: "Producto C", price: 45.2}
          ];

          this.updateParent();
      },

      remove(index) {
          this.items.splice(index, 1);

          this.updateParent();
      },

      updateParent() {
          let amount = 0;

            this.items.forEach(x => (amount += x.price));

            this.$emit("getValues", {
                amount: amount,
                quantity: this.items.length
            });
      }
  },

  mounted() {
      this.getAll();
  }
};
</script>

<style>
</style>