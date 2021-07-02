<template>
   
   <div>
     <navbar/>

   <header class="header">
      <searchBar/>
   </header>
   
   <main>
   <section class="category">
      <categorySection/>
   </section>

    <section  class="info-section">
      <infoSection/>
   </section>

   <section class="testimonial"> 
    <testimonial/>
   </section>

   <section class="featuredCountries">
     <featuredCountries/>
   </section >
   </main>
 </div>
</template>

<script>
import navbar from '../components/navbar';
import searchBar from '../components/searchBar';
import categorySection from '../components/categorySection';
import infoSection from '../components/infoSection';
import testimonial from '../components/testimonial';
import featuredCountries from '../components/featuredCountries';



export default {
   components:{
       navbar,
      searchBar,
      categorySection,
      infoSection,
      testimonial,
      featuredCountries
      
     
      
   }

}
</script>

<style>
  .header{
    background-image: url('../assets/images/kisspng-pingtan-county-property-real-estate-apartment-buil-vector-building-5a8d3abb0b55c9.6790646615192050510464.png');
    height: 80vh;
    background-repeat: no-repeat;
    margin-top: 60px;
  }

  .category{
    background-color: #F8F9FA;
    margin: 0px;
    padding: 40px 20px;
    height: 100vh;
  }

.info-section{
      height: 100vh;
}

  .testimonial{
    background-image: url('https://images.unsplash.com/photo-1603894499916-41df1f1750b9?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80');
    height: 100vh;
    background-repeat: no-repeat;
     background-size: cover;
     
    
  }

   .featuredCountries{
    background-color: #F8F9FA;
     padding: 20px;
   }
</style>