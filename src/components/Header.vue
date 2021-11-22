<template>
  <header>
    <div class="first_nav">
      <div class="my_cont">
        <div class="d-flex justify-content-between align-items-center">
          <ul>
            <li><i class="fa fa-facebook" aria-hidden="true"></i></li>
            <li><i class="fa fa-twitter" aria-hidden="true"></i></li>
            <li><i class="fa fa-instagram" aria-hidden="true"></i></li>
            <li><i class="fa fa-youtube-play" aria-hidden="true"></i></li>
          </ul>
          <ul class="cart_menu">
            <li>Shopping Cart</li>
            <li>My Account</li>
            <li class="cart">Cart</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="second_nav">
      <div class="my_cont">
        <div class="d-flex justify-content-between align-items-center">
          <img src="@/assets/classic_shop_logo1x.png" alt="" />
          <div>
            <ul class="cart_menu">
              <li>Home</li>
              <li>Home</li>
              <li>Home</li>
              <li>Home</li>
              <li>Home</li>
              <li>Home</li>
            </ul>
            <button>SHOP NOW!</button>
            <span><i class="fa fa-search" aria-hidden="true"></i></span>
          </div>
        </div>
      </div>
    </div>
    <div class="hero position-relative">
      <img src="@/assets/home1_slide_three_bg_2.jpg" width="100%" alt="" />
      <div class="hero_to_center">
        <div class="my_cont">
          <h1>Brand New Arrivals</h1>
          <p>NEW COLLECTION FROM NEW YORK</p>
          <button>VIEW ALL</button>
          <button>LOOKBOOK</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {},
};
</script>

<style lang="scss">
.first_nav {
  border-bottom: 1px solid grey;
  .my_cont {
    max-width: 1140px;
    margin: auto;
    ul {
      list-style: none;
      margin: 0;
      padding: 0;
      li {
        display: inline-block;
        i {
          padding: 10px;
        }
      }
    }
    .cart_menu {
      li {
        padding: 15px;
        border-right: 1px solid grey;
      }
      .cart {
        padding: 15px 60px 15px 60px;
      }
    }
  }
}
.second_nav {
  padding: 10px 0px;
  .my_cont {
    max-width: 1140px;
    margin: auto;
    ul {
      list-style: none;
      margin: 0;
      padding: 0;
    }
    .cart_menu {
      display: inline-block;
      li {
        padding: 20px;
        display: inline-block;
      }
    }
  }
}
.hero {
  /* background-image: url("../assets/home1_slide_three_bg_2.jpg");
  background-position: center;
  background-repeat: no-repeat; */
  .hero_to_center {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    .my_cont {
      max-width: 1140px;
      margin: auto;
      h1 {
        font-size: 80px;
        font-weight: bold;
        color: white;
      }
      p {
        color: white;
      }

      button {
        display: inline-block;
      }
    }
  }
}
</style>
