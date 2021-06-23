<template>
  <div class="search-form">
    <form class="form">
   <input type="search" placeholder="Where will you go">   
  
   <button class="button">Search</button>

   </form>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.search-form
 {
   color:#000000;
   display: flex;
   flex-wrap:wrap;
   flex-direction: column;
   align-items: center;
  
   
   
 }

.form{
   margin-top: 200px;
  padding: 6px;
  background-color: #f8f6f6e1;

}

input{
  border: 1px solid #0000004b;
  border-radius:10px ;
  width:700px;
  height:38px;

}

.button{
  padding:10px;
  width:100px;
background-color: #3bb78f;
background-image: linear-gradient(315deg, #3bb78f 0%, #0bab64 74%);

  border-radius:10px ;
}



</style>