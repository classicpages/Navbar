<template>
  <div class="bg-green-400 h-screen">
      <Navbar />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";


export default {
  name: "App",
  components: {
      Navbar,
  },
};
</script>