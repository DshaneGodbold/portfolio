<template>
<div>
    <NavBar class="navbar" />
    <router-view />
  </div>
  
</template>

<script>
import NavBar from "./components/NavBar.vue";

export default {
  components: { NavBar },
};
</script>

<style lang="scss">
.navbar {
  background-color: #2481ac;
}
</style>
