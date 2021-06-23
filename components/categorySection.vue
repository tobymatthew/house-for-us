<template>
  <div class="container">
    <div v-for="card in card" :key="card.id" class="card">
      <img :src="card.image" alt="" />
      <div class="card-container">
        <h4>{{ card.cityName }}</h4>
        <p>{{ card.listingNumber }}</p>
        <p>{{ card.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      card: [
        {
          image:
            "https://cdn.pixabay.com/photo/2012/11/17/16/03/mountains-66388__340.jpg",
          cityName: "Lagos",
          listingNumber: "14567",
          description:
            "A bustling expat, startup and nightlife scene where street food is the order of the day"
        },
        {
          image:
            "https://cdn.pixabay.com/photo/2012/11/17/16/03/mountains-66388__340.jpg",
          cityName: "Lagos",
          listingNumber: "14567",
          description:
            "A bustling expat, startup and nightlife scene where street food is the order of the day"
        },

        {
          image:
            "https://cdn.pixabay.com/photo/2012/11/17/16/03/mountains-66388__340.jpg",
          cityName: "Lagos",
          listingNumber: "14567",
          description:
            "A bustling expat, startup and nightlife scene where street food is the order of the day"
        }
      ]
    };
  }
};
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 1px 1px;
  grid-auto-flow: row;
  grid-template-areas:
    ". . ."
    ". . ."
    ". . .";
  margin: 100px 100px;
 
}

.card {
  /* Add shadows to create the "card" effect */
  background-color: #ffffff;
  border-radius: 4px;
  box-shadow: #000000 0px 1px 1px -1px;
  color: #000000;
  line-height: 24px;
  text-align: center;
  padding: 0px 0px 18px;
  width: 300px;
}



/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}



img{
  width: 300px;
}
</style>
