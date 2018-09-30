<template>
  <div id="app">
    <!-- Slots -->
    <appQuote>
        <h2 slot="title">Author: Mr.Me</h2>
        <h3 slot="title">{{ quoteTitle }}</h3>
        <p slot="content">Quote: A wonderful Quote</p>
    </appQuote>

    <!-- Dynamic Components -->
    <button @click="selectedComponent = 'app-quote'">Quote</button>
    <button @click="selectedComponent = 'app-author'">Author</button>
    <button @click="selectedComponent = 'app-new'">New</button>
    <hr>
    <p>{{ selectedComponent }}</p>
    <keep-alive>
      <component :is="selectedComponent">
        <p>Default Content</p>
      </component>
    </keep-alive>
  </div>
</template>

<script>
import AppQuote from "./components/Quote.vue";
import AppAuthor from "./components/Author";
import AppNew from "./components/New";
export default {
  name: "app",
  data() {
    return {
      quoteTitle: "Quote Title",
      selectedComponent: "app-quote"
    };
  },
  components: {
    appQuote: AppQuote,
    appAuthor: AppAuthor,
    appNew: AppNew
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
