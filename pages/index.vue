<template>
   
   <div>
     <navbar/>

   <header class="header">
      <searchBar/>
   </header>
   <section>
      <categorySection/>
   </section>
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
</style>