<template>
  <header>
    <div class="first_nav">
      <div class="my_cont">
        <div class="d-flex justify-content-between align-items-center">
          <SocialIcon></SocialIcon>
          <ul class="cart_menu">
            <li>Shopping Cart</li>
            <li>
              My Account <i class="fa fa-chevron-down" aria-hidden="true"></i>
            </li>
            <li class="cart">
              <i class="fa fa-shopping-cart" aria-hidden="true"></i>CART<i
                class="fa fa-chevron-down"
                aria-hidden="true"
              ></i>
            </li>
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
              <li v-for="(menuLink, i) in NavbarHeader" :key="i">
                {{ menuLink.title }}
                <i
                  v-if="!menuLink.subMenu ? `` : `d-none`"
                  class="fa fa-chevron-down sub_menu_icon"
                  aria-hidden="true"
                ></i>
              </li>
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
import SocialIcon from "./SocialIcon.vue";
export default {
  components: { SocialIcon },
  name: "Header",
  props: {},
  data() {
    return {
      NavbarHeader: [
        {
          title: "Home",
          subMenu: true,
        },
        {
          title: "Shop",
          subMenu: true,
        },
        {
          title: "Products",
          subMenu: true,
        },
        {
          title: "Categories",
          subMenu: true,
        },
        {
          title: "News",
          subMenu: false,
        },
        {
          title: "Elements",
          subMenu: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.first_nav {
  border-bottom: 1px solid #f6f6f6;
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
          font-size: 16px;
          padding-right: 20px;
        }
      }
    }
    .cart_menu {
      li {
        color: #6b6a6b;
        padding: 15px;
        border-right: 1px solid #f6f6f6;

        i {
          padding: 0px 10px;
          font-size: 10px;
        }
      }
      .cart {
        color: black;
        padding: 15px 60px 15px 60px;
        border: none;
        background-color: #fafafa;
        i {
          font-size: 18px;
          padding: 0px 10px;
        }
        .fa-chevron-down {
          font-size: 15px;
        }
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
        padding: 15px;
        display: inline-block;
        .sub_menu_icon {
          font-size: 13px;
          padding: 0px 5px;
        }
      }
    }
  }
}
.hero {
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
