<template>
  <NavBar />
  <DoraDiego />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import NavBar from "./components/NavBar.vue";
import DoraDiego from "./components/DoraDiego.vue";

@Options({
  components: {
    NavBar,
    DoraDiego
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
