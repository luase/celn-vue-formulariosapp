<template>
  <Navbar/>
  <div class="container">
    <router-view/>
  </div>
</template>

<script>
  import Navbar from "@/components/Navbar";

  export default {
    components: {
      Navbar
    }
  }
</script>

<style>
#nav a {
  font-weight: bold;
  color: #2c3e50;
}
</style>
