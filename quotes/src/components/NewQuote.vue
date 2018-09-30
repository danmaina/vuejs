<template>
    <div class="row">
      <div class="container-fluid">
          <form action="">
              <textarea v-model="quote" required class="form-control" 
                  id="" cols="30" rows="10" placeholder="Create New Quote" @keyup.enter.prevent="createQuote"></textarea>
          </form>
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      quote: ""
    };
  },
  methods: {
    createQuote() {
      console.log("quote added: " + this.quote);
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  }
};
</script>

<style>
</style>
