<template>
  <div>
    <div class="my-cont">
      <!-- ---------------------------------------------------FEATURED PRODUCT -->
      <section class="featured_products">
        <SectionTitle
          title="Featured Products"
          subtitle="Must have products from our top sellers"
        ></SectionTitle>
        <div>
          <ul class="filter_by_gender">
            <li>Men</li>
            <li>Women</li>
            <li>Accessories</li>
          </ul>
        </div>
        <div class="card_container">
          <div class="featured_products_card">
            <img src="@/assets/black_elegant_leather_jacket.jpg" alt="" />
            <p>Black Leather Jacket</p>
            <small>Men,Jackets,Jeans</small>
            <span>222</span>
            <span>121</span>
          </div>
          <div class="featured_products_card">
            <img src="@/assets/black_elegant_leather_jacket.jpg" alt="" />
            <p>Black Leather Jacket</p>
            <small>Men,Jackets,Jeans</small>
            <span>222</span>
            <span>121</span>
          </div>
          <div class="featured_products_card">
            <img src="@/assets/black_elegant_leather_jacket.jpg" alt="" />
            <p>Black Leather Jacket</p>
            <small>Men,Jackets,Jeans</small>
            <span>222</span>
            <span>121</span>
          </div>
          <div class="featured_products_card">
            <img src="@/assets/black_elegant_leather_jacket.jpg" alt="" />
            <p>Black Leather Jacket</p>
            <small>Men,Jackets,Jeans</small>
            <span>222</span>
            <span>121</span>
          </div>
        </div>
      </section>
      <!-- ---------------------------------------------------FEATURED PRODUCT -->
      <!--  -->
    </div>
    <div class="collection_section">
      <div class="collection_card">
        <!-- <img src="@/assets/winter_collection_bg.jpg" alt="" /> -->
        <div class="prova">
          <h3>Winter Collection</h3>
          <small>STYLISH AND WARM</small>
          <button>VIEW MORE</button>
        </div>
      </div>
      <!-- <div class="collection_card">
        <img src="@/assets/spring_collection_bg.jpg" alt="" />
        <h3>Spring Collection</h3>
        <small>BRIGHT AND COLORFUL</small>
        <button>VIEW MORE</button>
      </div>
      <div class="collection_card">
        <img src="@/assets/autumn_collection_bg.jpg" alt="" />
        <h3>Autumn Collection</h3>
        <small>RICH AND CONFORTABLE</small>
        <button>VIEW MORE</button>
      </div> -->
    </div>
    <!-- ------------------------------------------------------BEST SELLER SECTION -->
    <div class="bs_section">
      <div class="my_cont">
        <SectionTitle
          title="Best Seller"
          subtitle="Must have products from our top sellers"
        ></SectionTitle>
        <div class="container_bs">
          <div class="bs_card">
            <img src="../assets/spring_printed_dress.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <!-- ------------------------------------------------------------------------- -->
    <!-- ---------------------------------------BANNER OFFERTE SCONTO E FREE SHIPPING -->
    <div class="banner_offer">
      <div class="my_cont">
        <div class="offer_cont">
          <div class="offer_card_1">
            <div class="offer_card_content">
              <h2>70% Off</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <button>VIEW MORE</button>
            </div>
          </div>
          <div class="offer_card_2">
            <div class="offer_card_content">
              <h2>70% Off</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <button>VIEW MORE</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";
export default {
  components: { SectionTitle },
  name: "Header",
  props: {},
};
</script>

<style lang="scss">
@import "@/style/global.scss";
.my-cont {
  max-width: 1140px; //       !!DA ELIMINARE TUTTI I TAG MY_CONT!!    //
  margin: auto;
  .featured_products {
    padding: 70px 0px;

    .filter_by_gender {
      list-style: none;
      padding-left: 0;
      padding-bottom: 30px;
      margin: 0;

      li {
        display: inline-block;
        padding: 10px 50px;
        border: 1px solid grey;
      }
    }
    .card_container {
      display: flex;
      padding-bottom: 30px;
      .featured_products_card {
        width: calc(100% / 4);
        img {
          width: 100%;
        }
      }
    }
  }
}
.collection_section {
  display: flex;
  .collection_card {
    width: calc(100% / 3);
    background-image: url("../assets/winter_collection_bg.jpg");
    aspect-ratio: 1/1;
    background-position: top;
    position: relative;
    .prova {
      position: absolute;
      bottom: 20%;
      left: 50%;
      transform: translateX(-50%);
      h3 {
        font-size: 30px;
        color: white;
      }
      small {
        display: block;
      }
      button {
      }
    }
  }
}
.bs_section {
  padding: 70px 0px;
  .container_bs {
    .bs_card {
      width: calc(100% / 5);
      img {
        width: 100%;
      }
    }
  }
}
.banner_offer {
  height: 500px; //TEMPORANEO
  background-image: url("../assets/bkgd_confetti-compressor.jpg");
  background-position: center;
  .offer_card_1 {
    // --------------->   DA SISTEMARE!!!
    background-image: url("../assets/promo_box_1_bg.jpg");
  }
  .offer_card_2 {
    // --------------->   DA SISTEMARE!!!
    background-image: url("../assets/promo_box_2_bg.jpg");
  }
}
</style>
