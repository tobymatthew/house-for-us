<template>
  <div class="testimonial__container">
    <h2 class="testimonial__container--h2">This is Suzie. She just booked her <br> new home</h2>

    <p class="testimonial__container--p">
      “I was looking for a place for ages.   Then  I  discovered  <br>  HousingAnywhere 
      Within one week I found my new <br> home!”
    </p>

    <button class="testimonial__container--btn">FIND THE PERFECT PLACE</button>
  </div>
</template>

<script>
export default {};
</script>

<style>
.testimonial__container{
  height: inherit;
  display: flex;
 flex-direction: column;
 justify-content: center;
 align-items: flex-start;
 color: #fff;
 text-align: left;
 padding-left: 60px;
}

.testimonial__container--h2{
 font-family: Average sans;
 font-size: 45px;
 font-weight:800;
 margin-bottom: 16px;
}

.testimonial__container--p{
   font-size: 25px;
   line-height: 38px;
   margin-bottom: 15px;
}

.testimonial__container--btn{
  color: white;
  padding: 15px;
  border-radius: 5px;
  font-weight: bold;
  border: none;
  background-image: linear-gradient(315deg, #3bb78f 0%, #0bab64 74%);;
}

</style>
