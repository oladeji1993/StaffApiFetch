<template>
  <StaffList />
  <Fibonacci />
  <Palindrome />
</template>

<script>
import StaffList from "./components/StaffList.vue";
import Fibonacci from "./components/Fibonacci.vue";
import Palindrome from './components/palindrome.vue'


export default {
  name: "App",
  components: {
    StaffList,
    Fibonacci,
    Palindrome
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
</style>
