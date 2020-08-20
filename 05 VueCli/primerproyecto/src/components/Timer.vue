<template>
  <div>
    <span>Hora actual</span>: {{time}}
  </div>
</template>

<script>
export default {
  name: "timer",
  data() {
      return {
        time: '--'
      }
  },

  methods: {
    calcularTime() {
      setInterval(() => {
        let d = new Date();
        this.time = d.toLocaleTimeString();
      }, 1000);
    },
  },

  mounted() {
    this.calcularTime();
  },
};
</script>

<style>
</style>