<template>
  <div class="row">
    <Quote
      @click.native="deleteQuote(index)"
      v-for="(quote, index) in quotes"
      :key="index"
      >{{ quote }}</Quote
    >
  </div>
</template>

<script>
import Quote from "./Quote.vue";
export default {
  components: {
    Quote,
  },
  props: ["quotes"],
  methods: {
    deleteQuote(index) {
      this.$emit("deletedQuote", index);
    },
  },
};
</script>

<style scoped>
</style>