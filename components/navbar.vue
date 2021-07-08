<template>
  <div>
    <nav class="nav">
      <a class="nav-logo" href="">HouseForUs</a>
      <ul v-bind:class="{active:isActive}" class="nav-menu">
          
        <!-- <li class="nav-item_middle"><a class="nav-link"  href="">product</a></li>
        <li class="nav-item_middle"><a class="nav-link"  href="">pricing</a></li>
        <li class="nav-item_middle"><a class="nav-link"  href="">learn</a></li> -->
        
        <li class="nav-item"><a class="nav-link"  href="">LOG IN</a></li>
        <li class="nav-item"><a class="nav-link" href="">SIGN UP</a></li>
        <li class="nav-item"><a  class="nav-link last-child" href="">FOR LANLORDS</a></li>
      </ul>
      <div @click.prevent="toggle()" v-bind:class="{active:isActive}" class="hamburger">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return{
        isActive:false
    }
  },

  methods: {
        toggle(){
          this.isActive= !this.isActive
        }
  },
};
</script>

<style scoped>


li {
    list-style: none;
}

a {
    text-decoration: none;
}

.nav{
   border-bottom: 1px solid #E2E8F0;
   display: flex;
   justify-content: space-between;
   align-items: center;
   padding: 1rem 1.5rem;
}
.hamburger {
    display: none;
}

.bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: #101010;
}

.nav-menu {
    display: flex;
    align-items: center;
    margin-right: 20px ;
}

.nav-item {
    margin-left: 4rem;
}

/* .nav-item_middle{
    padding-right:150px;
    margin-right: 0px;
  
} */

.nav-link{
    font-size: 16px;
    font-weight:500;
    color: #000000;
    padding: 10px;
    text-transform: capitalize;

}

.nav-link:hover{
    background-color: #e3ecf5;
}


.nav-item:nth-child(3){
    border:1px solid #569c3cd7;
    border-radius: 5px;
    padding: 6px 10px;
}

.nav-item:nth-child(3):hover{
   background-color:#569c3c04;
   
}
.last-child:hover{
   background-color:transparent;
     color: #569c3cd7;
}

.nav-logo {
    font-size: 20px;
    color: #000000;
}

@media only screen and (max-width: 768px) {
    .nav-menu {
        position: fixed;
        left: -100%;
        top: 5rem;
        flex-direction: column;
        background-color: #fff;
        width: 100%;
        border-radius: 10px;
        text-align: center;
        transition: 0.3s;
        box-shadow:
            0 10px 27px rgba(0, 0, 0, 0.05);
    }

    .nav-menu.active {
        left: 0;
    }

    .nav-item {
        margin: 2.5rem 0;
    }
    .nav-item_middle{
         margin: 2.5rem 0;
    }

    .hamburger {
        display: block;
        cursor: pointer;
    }

     .hamburger.active .bar:nth-child(2) {
        opacity: 0;
    }

    .hamburger.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }

    .hamburger.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }


}

</style>
  