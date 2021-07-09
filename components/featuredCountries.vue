<template>
  <div>
    <h1 class="featuredCountries-header">
      Hundreds of cities around the world! Where will you go?
    </h1>
    <div class="featuredCountries-container">
      <div v-for="country in countries" :key="country.id">
        <p>{{ country.countryName }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      countries: [
        {
          countryName: "Spain"
        },
        {
          countryName: "Spain"
        },
        {
          countryName: "Spain"
        },
        {
          countryName: "Spain"
        },
        {
          countryName: "Spain"
        },
        {
          countryName: "Spain"
        },
        {
          countryName: "Spain"
        }
      ]
    };
  }
};
</script>

<style>
.featuredCountries-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  justify-content: space-evenly;
}

.featuredCountries-header {
  text-align: center;
  color: #2d4658;
  font-family: sans-serif;
  margin: 50px 0;
  font-size: 40px;
}
</style>
