<template>
  <div>
      <span class="icon">
          <i class="fa" :class="type"></i>
      </span>

      <span v-if="message">{{message}}</span>
  </div>
</template>

<script>
export default {
  name: "icon",

    props: {
        type: {
            type: String,
            required: true
        },

        message: {
            type: String
        }
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