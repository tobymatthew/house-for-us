<template>
  <div>
    <h1 class="category-header">Explore our most popular cities</h1>
    <p class="category-paragraph">
      See what these cities have to offer and rent the perfect place
    </p>

    <!-- <div class="category-container carousel-inner">
       <div class="card-carousel--nav__left" @click="moveCarousel(-1)" :disabled="atHeadOfList"></div>
      <div v-for="card in card" :key="card.id" class="card">
        <img :src="card.image" alt="" />
        <div class="card-container">
          <h4>{{ card.cityName }}</h4>
          <p>{{ card.listingNumber }}</p>
          <p>{{ card.description }}</p>
        </div>
      </div>
    </div> -->

      <div class="card-carousel-wrapper">
    <div class="card-carousel--nav__left" @click="moveCarousel(-1)" :disabled="atHeadOfList"></div>
    <div class="card-carousel">
      <div class="card-carousel--overflow-container">
        <div class="card-carousel-cards" :style="{ transform: 'translateX' + '(' + currentOffset + 'px' + ')'}">
          <div class="card-carousel--card" v-for="item in items" :key="item.id"><img src="https://cdn.pixabay.com/photo/2012/11/17/16/03/mountains-66388__340.jpg"/>
            <div class="card-carousel--card--footer">
              <p>{{ item.CityName }}</p>
              <!-- <p class="tag" v-for="(tag,index) in item.tag" :class="index &gt; 0 ? 'secondary' : ''">{{ tag }}</p> -->
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="card-carousel--nav__right" @click="moveCarousel(1)" :disabled="atEndOfList"></div>
  </div>
  </div>
</template>

<script>
import { Glide, GlideSlide } from "vue-glide-js";

export default {
  components: {
    [Glide.name]: Glide,
    [GlideSlide.name]: GlideSlide
  },

  data() {
    return {
      currentOffset: 0,
      windowSize: 3,
      paginationFactor: 220,

      items: [
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
  },
   computed: {
    atEndOfList() {
      return this.currentOffset <= (this.paginationFactor * -1) * (this.items.length - this.windowSize);
    },
    atHeadOfList() {
      return this.currentOffset === 0;
    },
  },
  methods: {
    moveCarousel(direction) {
      // Find a more elegant way to express the :style. consider using props to make it truly generic
      if (direction === 1 && !this.atEndOfList) {
        this.currentOffset -= this.paginationFactor;
      } else if (direction === -1 && !this.atHeadOfList) {
        this.currentOffset += this.paginationFactor;
      }
    },
  }


};
</script>

<style scoped>
.category-header,
.category-paragraph {
  text-align: center;
  color: #2d4658;
  font-family: sans-serif;
}

.category-header {
  font-size: 35px;
  margin: 20px;
}

.category-paragraph {
  color: #808f9a;
  margin-bottom: 45px;
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

img {
  width: 300px;
}



.card-carousel-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 20px 0 40px;
  color: #666a73;
}

.card-carousel {
  display: flex;
  justify-content: center;
  width: 640px;
}
.card-carousel--overflow-container {
  overflow: hidden;
}
.card-carousel--nav__left, .card-carousel--nav__right {
  display: inline-block;
  width: 15px;
  height: 15px;
  padding: 10px;
  box-sizing: border-box;
  border-top: 2px solid #42b883;
  border-right: 2px solid #42b883;
  cursor: pointer;
  margin: 0 20px;
  transition: transform 150ms linear;
}
.card-carousel--nav__left[disabled], .card-carousel--nav__right[disabled] {
  opacity: 0.2;
  border-color: black;
}
.card-carousel--nav__left {
  transform: rotate(-135deg);
}
.card-carousel--nav__left:active {
  transform: rotate(-135deg) scale(0.9);
}
.card-carousel--nav__right {
  transform: rotate(45deg);
}
.card-carousel--nav__right:active {
  transform: rotate(45deg) scale(0.9);
}

.card-carousel-cards {
  display: flex;
  transition: transform 150ms ease-out;
  transform: translatex(0px);
}
.card-carousel-cards .card-carousel--card {
  margin: 0 10px;
  cursor: pointer;
  box-shadow: 0 4px 15px 0 rgba(40, 44, 53, 0.06), 0 2px 2px 0 rgba(40, 44, 53, 0.08);
  background-color: #fff;
  border-radius: 4px;
  z-index: 3;
  margin-bottom: 2px;
}
.card-carousel-cards .card-carousel--card:first-child {
  margin-left: 0;
}
.card-carousel-cards .card-carousel--card:last-child {
  margin-right: 0;
}
.card-carousel-cards .card-carousel--card img {
  vertical-align: bottom;
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
  transition: opacity 150ms linear;
  user-select: none;
}
.card-carousel-cards .card-carousel--card img:hover {
  opacity: 0.5;
}
.card-carousel-cards .card-carousel--card--footer {
  border-top: 0;
  padding: 7px 15px;
}
.card-carousel-cards .card-carousel--card--footer p {
  padding: 3px 0;
  margin: 0;
  margin-bottom: 2px;
  font-size: 19px;
  font-weight: 500;
  color: #2c3e50;
  user-select: none;
}
.card-carousel-cards .card-carousel--card--footer p.tag {
  font-size: 11px;
  font-weight: 300;
  padding: 4px;
  background: rgba(40, 44, 53, 0.06);
  display: inline-block;
  position: relative;
  margin-left: 4px;
  color: #666a73;
}
.card-carousel-cards .card-carousel--card--footer p.tag:before {
  content: "";
  float: left;
  position: absolute;
  top: 0;
  left: -12px;
  width: 0;
  height: 0;
  border-color: transparent rgba(40, 44, 53, 0.06) transparent transparent;
  border-style: solid;
  border-width: 8px 12px 12px 0;
}
.card-carousel-cards .card-carousel--card--footer p.tag.secondary {
  margin-left: 0;
  border-left: 1.45px dashed white;
}
.card-carousel-cards .card-carousel--card--footer p.tag.secondary:before {
  display: none !important;
}
.card-carousel-cards .card-carousel--card--footer p.tag:after {
  content: "";
  position: absolute;
  top: 8px;
  left: -3px;
  float: left;
  width: 4px;
  height: 4px;
  border-radius: 2px;
  background: white;
  box-shadow: 0px 0px 0px #004977;
}

</style>
