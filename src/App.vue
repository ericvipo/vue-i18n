<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloI18n />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import HelloI18n from "./components/HelloI18n.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    HelloI18n,
  },
  created() {
    const locale = localStorage.getItem('locale')

    if(locale) {
      this.$root.$i18n.locale = locale
    } else if(navigator.language) {
      console.log('spanish rules!');
      this.$i18n.locale = navigator.language.substring(0, 2);
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
