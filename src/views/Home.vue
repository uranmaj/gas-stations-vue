<template>
  <div class="home">
    <!--<img alt="Vue logo" src="../assets/logo.png" />-->
    <Hero 
      title="To je tvoja bencinska postaja."
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut imperdiet urna purus. Integer mattis, magna placerat egestas rhoncus, ligula nisl consequat ex."
      action="Izvedi več" 
    />
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
