<template>
 <div class="header__container">
   <div class="text__container">
    <h1 class="header__text">Rent rooms, apartments <br> & stay for months</h1>
    </div>
  <div class="search-form">
    <form class="form">
      <input type="search" placeholder="Where will you go" />

      <button class="button">SEARCH</button>
    </form>
  </div>
 </div>
</template>

<script>
export default {};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Average+Sans&display=swap');
.header__container{
  height: inherit;
}

.text__container{
  padding-top:50px ;
}
.header__text{
  text-align: center;
  font-size: 65px;
  font-family: Average sans;
  background-image: linear-gradient(315deg, #3bb78f 0%, #10fa91 74%);
   background-clip: text;
  -webkit-text-fill-color: transparent;
  
}
.search-form {
  height: inherit;

  display: flex;

  /* flex-direction: column; */
  justify-content: center;
  align-items: center;
}

.form {
  margin-bottom: 300px;
  display: flex;
  flex-wrap: wrap;
  padding: 7px;
  background-color: #f8f6f6e1;
}

input {
  border: 1px solid #0000004b;
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  width: 700px;
  height: 45px;
}

.button {
  padding: 5px;
  width: 100px;
  color: #ffff;
  /* background-color: #3bb78f; */
  background-image: linear-gradient(315deg, #3bb78f 0%, #0bab64 74%);
  font-size:18px ;
  font-weight: 500;
  border: none;
  border-top-right-radius: 5px;
  border-bottom-right-radius:5px;
  
}
</style>
