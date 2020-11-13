<template>
  <div class="home">
    <!--<img alt="Vue logo" src="../assets/logo.png" />-->
    <Hero title="To je tvoja bencinska postaja." />
    <Stations/>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/Hero.vue";
import Stations from "@/components/Stations.vue";

export default {
  name: "Home",
  components: {
    Hero,
    Stations
  }
};
</script>
