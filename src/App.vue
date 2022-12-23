<template>
  <h1>{{ title }}</h1>
  <div>
    <input type="text" ref="name" />
    <button @click="handleClick">Click Me</button>
  </div>
</template>

<script>
export default {
  name: 'App',

  components: {},

  data() {
    return {
      title: 'Simple Modal App',
    };
  },

  methods: {
    handleClick() {
      console.log('name', this.$refs.name.value);

      // add class
      this.$refs.name.classList.add('active');

      // focus
      this.$refs.name.focus();
    },
  },
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

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
