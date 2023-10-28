<template>
  <NavBar />
  <Home />
  <FooterComponent />
</template>

<script>
import Home from "./components/Home.vue";
import NavBar from "./components/NavBar.vue";
import FooterComponent from "./components/FooterComponent.vue";
export default {
  name: "App",
  components: {
    NavBar,
    Home,
    FooterComponent,
  },
};
</script>
<style>
body {
  margin: 0;
  padding: 0;
}
::-webkit-scrollbar {
  display: none;
}
a{
    text-decoration: none;
    color:black;
}
</style>
