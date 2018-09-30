<template>
    <div class="row">
        <new-quote @quoteAdded="createNewQuote"></new-quote>
        <hr>
        <app-quote v-for="quote in quotes" :key="quote">{{ quote }}</app-quote>
    </div>
</template>

<script>
import Quote from "./Quote.vue";
import NewQuote from "./NewQuote.vue";
export default {
  props: ["quotes"],
  components: {
    newQuote: NewQuote,
    appQuote: Quote
  },
  methods: {
    createNewQuote(quote) {
      this.quotes.push(quote);
    }
  }
};
</script>
<style>
</style>
