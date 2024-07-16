<template>
  <input type="text" v-model="query" @input="search" placeholder="Search for TV shows..." />
</template>

<script>
export default {
  data() {
    return {
      query: ''
    };
  },
  methods: {
    search() {
      this.$emit('search', this.query);
    }
  }
};
</script>
