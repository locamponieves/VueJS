<template>
  <section class="content">
      <div class="title">{{title}}</div>

      <slot></slot>
  </section>
</template>

<script>
export default {
  name: "page",

    props: {
        title: String
    },

  data() {
      return {
      }
  },

  methods: {
  },

  mounted() {
  }
};
</script>

<style>
</style>