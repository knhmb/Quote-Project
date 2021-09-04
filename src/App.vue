<template>
  <div class="container">
    <Header :quotesCount="quotes.length" :maxQuotes="maxQuotes" />
    <new-quote @addedQuote="quoteAdded"></new-quote>
    <quote-grid @deletedQuote="deletedQuote" :quotes="quotes"></quote-grid>
    <div class="row">
      <div class="col-sm-12">
        <div class="alert alert-info text-center">
          Info: Click to delete a quote.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import Header from "./components/Header.vue";

export default {
  components: {
    QuoteGrid,
    NewQuote,
    Header,
  },
  data() {
    return {
      maxQuotes: 10,
      quotes: ["Just a quote to show something"],
    };
  },
  methods: {
    quoteAdded(quote) {
      if (this.quotes.length >= 10) {
        alert("Delete a quote to add a new one!");
      } else {
        this.quotes.push(quote);
      }
    },
    deletedQuote(index) {
      this.quotes.splice(index, 1);
    },
  },
};
</script>

<style>
</style>
