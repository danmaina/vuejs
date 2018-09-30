<template>
  <div class="row">
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <new-quote @quoteAdded="createNewQuote"></new-quote>
        <hr>
        <app-quote-grid :quotes="quotes" @quoteToDelete="deleteQuote"></app-quote-grid>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import AppHeader from "./components/Header.vue";
export default {
  data: function() {
    return {
      maxQuotes: 10,
      quotes: [
        "We Do not rise to the level of our expectations, we fall to the level of our training."
      ]
    };
  },
  components: {
    appHeader: AppHeader,
    newQuote: NewQuote,
    appQuoteGrid: QuoteGrid
  },
  methods: {
    createNewQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert(
          "You have reached the maximum number of quotes allowed: " +
            this.maxQuotes
        );
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style scoped>
.row {
  margin-top: 15px;
}
</style>
