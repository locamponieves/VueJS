<template>
  <span>{{amountFormat}}</span>
</template>

<script>
export default {
  name: "currency",

  props: {
    amount: {
      type: Number,
      required: true
    },

    culture: String,
  },

  data() {
    return {
      currencies: [
        { culture: "es-PE", style: "PEN", value: 3.5 },
        { culture: "es-USD", style: "USD", value: 1 },
        { culture: "es-MX", style: "MXN", value: 19.08 },
      ],
    };
  },

  computed: {
    amountFormat() {
      let currency = this.currencies.find((x) => x.culture === this.culture);

      return (this.amount * currency.value).toLocaleString(currency.culture, {
        style: "currency",
        currency: currency.style,
      });
    },
  },

  methods: {},

  mounted() {},
};
</script>

<style>
</style>