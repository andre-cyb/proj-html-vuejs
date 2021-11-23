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
          <div
            class="featured_products_card"
            v-for="(product, i) in maleCollection"
            :key="i"
          >
            <img :src="product.image" alt="" />
            <p>{{ product.product }}</p>
            <small>{{ product.tags }}</small>
            <span :class="product.oldPrice ? `d-block` : `d-none`">
              {{ product.oldPrice }}</span
            >
            <span>{{ product.price }}</span>
          </div>
        </div>
      </section>
      <!-- --------------------------------------------------------------------- -->
      <!-- -------------------------------------------------------COLLECTION  -->
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
          <div
            class="bs_card"
            v-for="(BsCard, i) in bestSeller"
            :key="`BestS` + i"
          >
            <img :src="BsCard.image" alt="" />
          </div>
        </div>
      </div>
    </div>
    <!-- ------------------------------------------------------------------------- -->
    <!-- ---------------------------------------BANNER OFFERTE SCONTO E FREE SHIPPING -->
    <!-- FARE COMPONENTE CON PROPS !!!!!!!!!!!!!!!!! -->
    <div class="banner_offer">
      <div class="my_cont">
        <div class="offer_cont">
          <div class="offer_card_1 text-white">
            <img src="@/assets/promo_box_1_bg.jpg" width="100%" alt="" />
            <div class="offer_card_content">
              <h2>70% Off</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <button>VIEW MORE</button>
            </div>
          </div>
          <div class="offer_card_1 text-white">
            <img src="@/assets/promo_box_1_bg.jpg" width="100%" alt="" />
            <div class="offer_card_content">
              <h2>70% Off</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <button>VIEW MORE</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- -------------------------------------------------------------------------- -->
    <!-- ---------------------------------------------------------SEZIONE NEW ARRIVALS -->
    <div class="na_section">
      <SectionTitle
        class="my_cont"
        title="New Arrivals"
        subtitle="Must have products from our top sellers"
      ></SectionTitle>

      <div class="container_na">
        <div
          class="na_card"
          v-for="(NaCard, i) in NewArrivals"
          :key="`NastS` + i"
        >
          <img :src="NaCard.image" width="100%" alt="" />
        </div>
      </div>
    </div>
    <!-- -------------------------------------------------------------------------- -->
    <!-- ---------------------------------------------------------BANNER RECENSIONE -->
    <div class="banner_testimonial">
      <div class="my_cont">
        <div class="testimonial_cont">
          <img src="../assets/man_testimonial.png" alt="" />
          <p class="p-4">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nam,
            excepturi veniam quo quod, adipisci necessitatibus commodi, animi
            perferendis maxime aliquam architecto. Mollitia ratione cupiditate
            rem, quidem tempore sint consequuntur labore?
          </p>
          <span><strong>Dario Pineda</strong>, Theme Fusion</span>
          <div>1/2</div>
        </div>
      </div>
    </div>
    <!-- ----------------------------------------------------------------------------- -->
    <!-- ---------------------------------------------------------SEZIONE FROM OUR BLOG -->
    <div class="from_blog_section">
      <div class="my_cont">
        <SectionTitle
          title="From Our Blog"
          subtitle="Must have products from our top sellers"
        ></SectionTitle>
        <div class="container_from_blog">
          <div
            class="from_blog_card"
            v-for="(FbCard, i) in fromBlog"
            :key="`BlogCard` + i"
          >
            <img :src="FbCard.thumb" alt="" />
            <div>
              <p>{{ FbCard.title }}</p>
              <small>September 9th, 2015 | 0 Comments</small>
            </div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa
            </p>
          </div>
        </div>
      </div>
    </div>
    <!-- ----------------------------------------------------------------------------- -->
    <hr />
    <!-- ---------------------------------------------------------SEZIONE PREVIEW ITEMS -->
    <div class="preview_items">
      <div class="my_cont">
        <div class="row">
          <PreviewItem title="FEATURED"></PreviewItem>
          <PreviewItem title="FEATURED"></PreviewItem>
          <PreviewItem title="FEATURED"></PreviewItem>
          <PreviewItem title="FEATURED"></PreviewItem>
        </div>
      </div>
    </div>
    <!-- ----------------------------------------------------------------------------- -->
    <!-- ---------------------------------------------------------SEZIONE LOGHI BRAND -->
    <div class="logo_section">
      <div class="my_cont">
        <p>BRAND LOGOS</p>
        <div class="logos_container">
          <div class="logo">
            <img src="../assets/b_logotype_6.png" alt="" />
          </div>
          <div class="logo">
            <img src="../assets/b_logotype_7.png" alt="" />
          </div>
          <div class="logo">
            <img src="../assets/b_logotype_1.png" alt="" />
          </div>
          <div class="logo">
            <img src="../assets/b_logotype_2.png" alt="" />
          </div>
          <div class="logo">
            <img src="../assets/b_logotype_3.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PreviewItem from "./PreviewItem.vue";
import SectionTitle from "./SectionTitle.vue";
export default {
  components: { SectionTitle, PreviewItem },
  name: "Header",
  props: {},
  data() {
    return {
      maleCollection: [
        {
          product: "Black Leather Jacket",
          tags: "Men, Jackets, Jeans", //  ------------------------------- !!SE RIMANE TEMPO CREA UN ARRAY PER I TAG  //
          price: "$121",
          discount: true,
          oldPrice: "$235",
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
        },
        {
          product: "Black Leather Suit",
          tags: "Men, Jackets", //  ------------------------------- !!SE RIMANE TEMPO CREA UN ARRAY PER I TAG  //
          price: "$176",
          discount: false,
          oldPrice: "",
          image: require("@/assets/black_leather_suit.jpg"),
        },
        {
          product: "Blue Jacket & Stripe Tee",
          tags: "Men, Jackets, Suits", //  ------------------------------- !!SE RIMANE TEMPO CREA UN ARRAY PER I TAG  //
          price: "$580",
          discount: false,
          oldPrice: "",
          image: require("@/assets/blue_jacket_and_white_stripe_tee.jpg"),
        },
        {
          product: "Modern Black Leather suit",
          tags: "Men, Jackets", //  ------------------------------- !!SE RIMANE TEMPO CREA UN ARRAY PER I TAG  //
          price: "$96",
          discount: false,
          oldPrice: "",
          image: require("@/assets/modern_black_leather_suit.jpg"),
        },
      ],
      bestSeller: [
        {
          image: require("@/assets/spring_printed_dress.jpg"),
        },
        {
          image: require("@/assets/modern_love_tee.jpg"),
        },
        {
          image: require("@/assets/black_leather_jacket.jpg"),
        },
        {
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
        },
        {
          image: require("@/assets/hipster_black_top.jpg"),
        },
      ],
      NewArrivals: [
        {
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
        },
        {
          image: require("@/assets/hipster_black_top.jpg"),
        },
        {
          image: require("@/assets/black_leather_suit.jpg"),
        },
        {
          image: require("@/assets/spring_printed_dress.jpg"),
        },
        {
          image: require("@/assets/modern_love_tee.jpg"),
        },
      ],
      fromBlog: [
        {
          title: "Integer ac felis aliquet dignissim",
          thumb: require("@/assets/post_img_12-700x441.jpg"),
        },
        {
          title: "sagittis iaculis id justo",
          thumb: require("@/assets/post_img_11-700x441.jpg"),
        },
        {
          title: "Sollicitudin nulla facilisi nisl curae",
          thumb: require("@/assets/post_img_10-700x441.jpg"),
        },
      ],
    };
  },
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
    }
  }
}
.bs_section {
  padding: 70px 0px;
  .container_bs {
    display: flex;
    .bs_card {
      width: calc(100% / 5);
      img {
        width: 100%;
      }
    }
  }
}
.banner_offer {
  display: flex;
  padding: 70px 0px;
  background-image: url("../assets/bkgd_confetti-compressor.jpg");
  background-position: center;

  .offer_cont {
    display: flex;
    justify-content: space-between;
    height: 300px;
    width: 1140px;
    .offer_card_1 {
      width: 45%;
      position: relative;
      img {
        width: 100%;
        height: 100%;
      }
      .offer_card_content {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        text-align: start;
        padding-left: 50px;
      }
    }
    .offer_card_2 {
      width: 45%;
      background-image: url("../assets/promo_box_2_bg.jpg");
    }
  }
}
.na_section {
  padding: 70px 0px;
  .container_na {
    display: flex;
    .na_card {
      width: calc(100% / 5);
    }
  }
}
.banner_testimonial {
  background-image: url("../assets/testimonials_home_1_bg.jpg");
  padding: 100px 0px;
  color: white;

  p {
    padding: 20px 110px;
    font-style: italic;
  }
}
.from_blog_section {
  padding: 70px 0px;
  .container_from_blog {
    display: flex;
    .from_blog_card {
      width: calc(100% / 3);
      text-align: start;
      img {
        width: 100%;
      }
      div {
        padding-top: 10px;
        padding-bottom: 20px;
        p {
          font-weight: bold;
        }
      }
      p {
        margin: 0;
      }
    }
  }
}
.preview_items {
  padding: 70px 0px;
  text-align: start;
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
    li {
      padding: 10px 0px;
      display: flex;
      border-bottom: 1px solid rgb(184, 184, 184);
      .item_details {
        width: 80%;
      }
      .item_image {
        width: 20%;
      }
    }
  }
}
.logo_section {
  padding: 70px 0px;
  background-color: #e7e7e7;
  .logos_container {
    display: flex;
    .logo {
      width: calc(100% / 5);
    }
  }
}
</style>
