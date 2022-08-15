<template>
  <div>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/skills">About Me</router-link> |
      <router-link to="/resume">Resume</router-link> |
    </nav>
  <router-view/>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<style>

</style>
