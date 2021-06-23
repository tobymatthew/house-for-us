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
.contianer {
  display: inline-grid;
  grid-template-columns: 1fr 1fr 1fr;
}

.card {
  /* Add shadows to create the "card" effect */

  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.card-container {
  padding: 2px 16px;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  border-radius: 5px; /* 5px rounded corners */
}

/* Add rounded corners to the top left and the top right corner of the image */
img {
  border-radius: 5px 5px 0 0;
}
</style>
