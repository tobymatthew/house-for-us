<template>
  <div>
    <h1 class="category-header">Explore our most popular cities</h1>
    <p class="category-paragraph">See what these cities have to offer and rent the perfect place</p>
  <div class="category-container">
    
    <div v-for="card in card" :key="card.id" class="card">
      <img :src="card.image" alt="" />
      <div class="card-container">
        <h4>{{ card.cityName }}</h4>
        <p>{{ card.listingNumber }}</p>
        <p>{{ card.description }}</p>
      </div>
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

  .category-header,.category-paragraph{
   text-align: center;
    color: #2d4658;
    font-family: sans-serif;

  }

   .category-header{
     font-size: 35px;
     margin:20px;
   }

   .category-paragraph{
     color:#808f9a;
      margin-bottom:45px;
   }
.category-container {
 height: inherit;
 display: flex;
 flex-wrap: wrap;
 justify-content: center;
 justify-content: space-evenly;
 padding-bottom: 50px;
 align-items: center;
 
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
  height: 350px;
  margin-bottom: 10px;
  
}



/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}



img{
  width: 300px;
}
</style>
