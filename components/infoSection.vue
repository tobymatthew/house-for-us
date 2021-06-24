<template>
  <div class="container">
    <div v-for="card in card" :key="card.id" class="card">
      <img :src="card.image" alt="" />
      <div class="card-container">
        <h4>{{ card.cityName }}</h4>
        
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
            "https://thumb.housinganywhere.com/dist/tenant-1-b51ad9261a4b09df2cf9.bundle.svg",
          cityName: "Search fast, search smart",
          
          description:
            "Browse hundreds of properties in your city of choice. Save your favorites and set up search alerts so you don't miss your dream place!"
        },
        {
          image:
            "data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNDkiIGhlaWdodD0iMTExIj48ZGVmcz48bGluZWFyR3JhZGllbnQgaWQ9ImEiIHgxPSIuNSIgeTE9IjEiIHgyPSIuNSIgZ3JhZGllbnRVbml0cz0ib2JqZWN0Qm91bmRpbmdCb3giPjxzdG9wIG9mZnNldD0iMCIgc3RvcC1jb2xvcj0iZ3JheSIgc3RvcC1vcGFjaXR5PSIuMjUxIi8+PHN0b3Agb2Zmc2V0PSIuNTQiIHN0b3AtY29sb3I9ImdyYXkiIHN0b3Atb3BhY2l0eT0iLjEyMiIvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iZ3JheSIgc3RvcC1vcGFjaXR5PSIuMTAyIi8+PC9saW5lYXJHcmFkaWVudD48bGluZWFyR3JhZGllbnQgaWQ9ImIiIHgxPSIuMjM1IiB5MT0iLjUiIHgyPSIuNzU4IiB5Mj0iMS4zMTgiIGdyYWRpZW50VW5pdHM9Im9iamVjdEJvdW5kaW5nQm94Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiNmYTcwMDkiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNmZmJjMGQiLz48L2xpbmVhckdyYWRpZW50PjwvZGVmcz48cGF0aCBkPSJNMCAwaDEwMXY3My40ODNIMzYuNzgzTDI5Ljg0NSA4NmwtNy4yODktMTIuNTE3SDBWMHoiIGZpbGw9InVybCgjYSkiLz48cGF0aCBkYXRhLW5hbWU9IlBhdGgiIGQ9Ik0xIDFoOTh2NzEuMjEzSDM1LjM5M0wyOS41IDg1bC02LjYxNS0xMi43ODdIMVYxeiIgZmlsbD0iI2Y1ZjVmNSIvPjxwYXRoIGZpbGw9IiM5MjUzODYiIG9wYWNpdHk9Ii4zIiBkPSJNODcgMjZIMTR2LTNoNzN6Ii8+PHBhdGggZGF0YS1uYW1lPSJSZWN0YW5nbGUiIGZpbGw9IiM5MjUzODYiIG9wYWNpdHk9Ii4zIiBkPSJNODcgMzNIMTR2LTNoNzN6TTg3IDM5SDE0di0zaDczek04NyA0NkgxNHYtM2g3M3oiLz48cGF0aCBkYXRhLW5hbWU9IlBhdGgiIGQ9Ik0xMDAgMEgwdjczLjQ4M2w2NC41MjctLjAzNkw3MC42MDggODZsNy4wNTktMTIuNTE3SDEwMFYweiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDkgMjUpIiBmaWxsPSJ1cmwoI2EpIi8+PHBhdGggZGF0YS1uYW1lPSJQYXRoIiBkPSJNMTQ4IDI2SDUwdjcxLjIxM2g2My42MDdMMTE5LjUgMTEwbDYuNjE3LTEyLjc4N0gxNDhWMjZ6IiBmaWxsPSIjZmZmIi8+PGNpcmNsZSBjeD0iNyIgY3k9IjciIHI9IjciIHRyYW5zZm9ybT0idHJhbnNsYXRlKDc0IDU1KSIgZmlsbD0idXJsKCNhKSIvPjxjaXJjbGUgZGF0YS1uYW1lPSJPdmFsIiBjeD0iNyIgY3k9IjciIHI9IjciIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkyIDU1KSIgZmlsbD0idXJsKCNhKSIvPjxjaXJjbGUgZGF0YS1uYW1lPSJPdmFsIiBjeD0iNyIgY3k9IjciIHI9IjciIHRyYW5zZm9ybT0idHJhbnNsYXRlKDExMCA1NSkiIGZpbGw9InVybCgjYSkiLz48Y2lyY2xlIGRhdGEtbmFtZT0iT3ZhbCIgY3g9IjYuNSIgY3k9IjYuNSIgcj0iNi41IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg3NSA1NSkiIGZpbGw9InVybCgjYikiLz48Y2lyY2xlIGRhdGEtbmFtZT0iT3ZhbCIgY3g9IjYuNSIgY3k9IjYuNSIgcj0iNi41IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg5MyA1NSkiIGZpbGw9IiNmZjgxMjciIG9wYWNpdHk9Ii41Ii8+PGNpcmNsZSBkYXRhLW5hbWU9Ik92YWwiIGN4PSI2LjUiIGN5PSI2LjUiIHI9IjYuNSIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTExIDU1KSIgZmlsbD0iI2ZmODEyNyIgb3BhY2l0eT0iLjIiLz48L3N2Zz4=",
          cityName: "Real-time chat with real people",
          
          description:
            "Communicate directly with advertisers. If all goes well, one of these verified users will become your new landlord!"
        },

        {
          image:
            "https://thumb.housinganywhere.com/dist/tenant-3-e283200aa0fea31c1431.bundle.svg",
          cityName: "Book and pay online, securely",
       
          description:
            "Once you pay the first’s month rent, the place is yours. We protect your money and transfer it to the landlord only 48 hours after you’ve moved-in"
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
