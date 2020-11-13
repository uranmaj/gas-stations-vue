<template>
  <div class="hero">
    <section id="hero" role="main" title="Gas Station">
      <div class="container">
        <b-col cols="12" lg="9" class="pb-4 pl-0"><h1>{{ title }}</h1></b-col>
        <b-col cols="8" lg="6" class="pb-4 pl-0"><p>{{ description }}</p></b-col> 
        <b-button href="about" class="btn btn-lg btn-light cta" role="button">{{ action }}</b-button> 
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Hero",
  props: {
    title: String,
    description: String,
    action: String
  }
};
</script>

<style lang="scss">

@import "../assets/styles/_variables.scss";
@import "../assets/styles/global.scss";

#hero {
  background: url("../assets/images/gas.jpg") no-repeat right top;
  background-size: auto 60vh;
  background-position-y: 3rem;
  padding-top: 5rem;
  padding-bottom: 5rem;
  .cta {
    background-color: $station-red;
  }
}

@media (max-width: 1050px) { 
  #hero {
    padding-top: 2rem;
    padding-bottom: 5rem;
    background-size: auto 50vh;
    background-position-x: 50vw;
    h1 {
      font-size:50px;
      line-height: 1;      
    }
  }
}

.cta-sm {
  font-size: 16px;
  font-weight: bold;
  color: #ffffff;
}

#station-accordion .card-header:hover {
  background-color: #f1f1f1;
}
.station-list {
  padding-top: 5rem;
  padding-bottom: 5rem;
}
.station-list .cta {
  background-color: #C4CB4B;
}

.fa-star {
  color: #666666;
}
.checked {
  color: #FFCC00;
}

</style>