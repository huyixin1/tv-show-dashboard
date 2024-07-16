<template>
  <div id="app">
    <header>
      <h1>TV Show Dashboard</h1>
      <SearchBar @search="handleSearch" />
    </header>
    <router-view :key="$route.fullPath" />
  </div>
</template>

<script>
import SearchBar from './components/SearchBar.vue';

export default {
  components: {
    SearchBar
  },
  methods: {
    handleSearch(query) {
      // You can handle search queries here if needed
      console.log(query);
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

header {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 20px;
}

h1 {
  margin: 0;
}
</style>
