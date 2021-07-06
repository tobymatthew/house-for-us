<template>
  <div>
    <h1 class="featuredCities__header">Featured countries</h1>
    <div class="featuredCities__container">
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

<style scoped>

.featuredCities__header{
    text-align: center;
    margin: 20px;
}

.featuredCities__container{
    display:grid ;
    grid-template-columns: repeat(7,1fr);
    gap: 10px;
}

</style>
