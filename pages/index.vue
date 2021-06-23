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

    <section >
      <categorySection/>
   </section>
   </main>
 </div>
</template>

<script>
import navbar from '../components/navbar';
import searchBar from '../components/searchBar';
import categorySection from '../components/categorySection';

export default {
   components:{
       navbar,
      searchBar,
      categorySection
      
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
</style>