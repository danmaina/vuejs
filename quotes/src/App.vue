<template>
    <div class="container">
        <div>
            <h1>Quotes</h1>
        </div>
        <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
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
    appQuoteGrid: QuoteGrid
  }
};
</script>

<style scoped>
</style>
