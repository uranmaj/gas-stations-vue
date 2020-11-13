<template>
<section id="station-list" class="bg-light">
  <!-- all gas stations - list SECTION -->
  <div class="container">

    <!-- gas station filter menu -->
    <div class="container px-0 mb-4">
      <b-row>
        <!-- simple javascript autocomplete -->
        <b-col xs="12" lg="4">
          <label class="sr-only" for="kraj">Ime kraja..</label>
          <b-input-group prepend="Kraj">
            <b-form-input id="kraj" placeholder="Ime kraja.."></b-form-input>
          </b-input-group>
        </b-col>
        <!-- checkboxes -->
        <b-col xs="12" lg="4" class="text-center">
          <b-form-checkbox-group id="dodaten-tip-goriva" class="text-center my-auto">
            <b-form-checkbox value="Elektirka">Elektrika</b-form-checkbox>
            <b-form-checkbox value="Plin">Plin</b-form-checkbox>
          </b-form-checkbox-group>
        </b-col>
        <b-col xs="12" lg="4">
        <!-- select options -->
        <b-form-select v-model="selected" :options="options"></b-form-select>
        </b-col>
      </b-row>
    </div>

    <!-- accordion -->
      <div class="accordion" role="tablist">
    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-0" role="tab">
        <b-button block v-b-toggle.accordion-1 >Accordion 1</b-button>
      </b-card-header>
      <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
        <b-card-body>
 
        </b-card-body>
      </b-collapse>
    </b-card>
    </div>

  </div>
</section>
</template>

<script>
export default {
  name: "Stations",
  data() {
      return {
        selected: 'a',
        options: [
          { value: 'a', text: 'Najbolj priljubljeni' },
          { value: 'b', text: 'Najbližji' },
          { value: 'c', text: 'Cenejši naprej' },
          { value: 'd', text: 'Dražji naprej' },
          { value: 'e', text: 'Najbolje ocenjeni' }
        ]
      }
    }
};
</script>

<style scoped lang="scss">

@import "../assets/styles/_variables.scss";
@import "../assets/styles/global.scss";

.input-group-text {
  font-weight:bold;
}

.cta-sm {
  font-size: 16px;
  font-weight: bold;
  color: #ffffff;
}

#station-accordion .card-header:hover {
  background-color: #f1f1f1;
}
#station-list {
  padding-top: 5rem;
  padding-bottom: 5rem;
}
#station-list .cta {
  background-color: #C4CB4B;
}

.fa-star {
  color: #666666;
}
.checked {
  color: #FFCC00;
}

</style>
