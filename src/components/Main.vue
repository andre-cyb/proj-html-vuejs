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
            <li class="active">Men</li>
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
            <div class="price_cont">
              <span
                class="d-price"
                :class="product.oldPrice ? `d-inline-block` : `d-none`"
              >
                {{ product.oldPrice }}</span
              >
              <span class="price">{{ product.price }}</span>
            </div>
          </div>
        </div>
      </section>
      <!-- --------------------------------------------------------------------- -->
      <!-- -------------------------------------------------------COLLECTION  -->
    </div>
    <div class="collection_section">
      <div class="collection_card">
        <img src="@/assets/winter_collection_bg.jpg" alt="" />
        <div class="card_content">
          <h3>Winter Collection</h3>
          <small>STYLISH AND WARM</small>
          <button class="btn btn-outline-light my_light_btn">VIEW MORE</button>
        </div>
      </div>
      <div class="collection_card">
        <img src="@/assets/spring_collection_bg.jpg" alt="" />
        <div class="card_content">
          <h3>Spring Collection</h3>
          <small>BRIGHT AND COLORFUL</small>
          <button class="btn btn-outline-light my_light_btn">VIEW MORE</button>
        </div>
      </div>
      <div class="collection_card">
        <img src="@/assets/autumn_collection_bg.jpg" alt="" />
        <div class="card_content">
          <h3>Autumn Collection</h3>
          <small>RICH AND COMFORTABLE</small>
          <button class="btn btn-outline-light my_light_btn">VIEW MORE</button>
        </div>
      </div>
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
          <span class="arrow_style" style="right: 0"
            ><i class="fa fa-chevron-right" aria-hidden="true"></i
          ></span>
          <span class="arrow_style" style="left: 0"
            ><i class="fa fa-chevron-left" aria-hidden="true"></i
          ></span>
        </div>
      </div>
    </div>
    <!-- ------------------------------------------------------------------------- -->
    <!-- ---------------------------------------BANNER OFFERTE SCONTO E FREE SHIPPING -->
    <!-- FARE COMPONENTE CON PROPS !!!!!!!!!!!!!!!!! -->
    <div class="banner_offer">
      <div class="my_cont">
        <div class="offer_cont">
          <!--  <BannerOffer
            image="@/assets/promo_box_1_bg.jpg"
            offer="70% Off"
            text="Lorem ipsum dolor sit amet consectetur adipisicing elit."
          ></BannerOffer> -->
          <div class="offer_card text-white">
            <img src="@/assets/promo_box_1_bg.jpg" width="100%" alt="" />
            <div class="offer_card_content">
              <h1>70% Off</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
              <button class="btn btn-outline-light my_light_btn">
                VIEW MORE
              </button>
            </div>
          </div>
          <div class="offer_card text-white">
            <img src="@/assets/promo_box_2_bg.jpg" width="100%" alt="" />
            <div class="offer_card_content">
              <h1>Free Shipping</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
              <button class="btn btn-outline-light my_light_btn">
                VIEW MORE
              </button>
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
        <span class="arrow_style" style="right: 0"
          ><i class="fa fa-chevron-right" aria-hidden="true"></i
        ></span>
        <span class="arrow_style" style="left: 0"
          ><i class="fa fa-chevron-left" aria-hidden="true"></i
        ></span>
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
          class="pt-3 pb-3"
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
          <PreviewItem title="FEATURED" :Arr="featured"></PreviewItem>
          <PreviewItem title="ON SALE" :Arr="onSale"></PreviewItem>
          <PreviewItem title="TOP RATED" :Arr="topRated"></PreviewItem>
          <PreviewItem
            title="LATEST REVIEWS"
            :Arr="latestReviews"
          ></PreviewItem>
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
//import BannerOffer from "./BannerOffer.vue";
import PreviewItem from "./PreviewItem.vue";
import SectionTitle from "./SectionTitle.vue";
export default {
  components: { SectionTitle, PreviewItem /* BannerOffer */ },
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
      featured: [
        {
          image: require("@/assets/black_leather_jacket.jpg"),
          title: "Black Jacket",
          oldPrice: 0,
          price: 125,
          vote: 0,
          brand: "",
        },
        {
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
          title: "Black Leather Jacket",
          oldPrice: 235,
          price: 200,
          vote: 5,
          brand: "",
        },
        {
          image: require("@/assets/hipster_black_top.jpg"),
          title: "Hipster Black Top",
          oldPrice: 0,
          price: 57,
          vote: 0,
          brand: "",
        },
      ],
      onSale: [
        {
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
          title: "Black Leather Jacket",
          oldPrice: 235,
          price: 200,
          vote: 5,
          brand: "",
        },
        {
          image: require("@/assets/blue_leather_jacket-400x520.jpg"),
          title: "Blue Leather Jacket",
          oldPrice: 80,
          price: 60,
          vote: 0,
          brand: "",
        },
        {
          image: require("@/assets/modern_leather_boots-400x520.jpg"),
          title: "Modern Leather Boots",
          oldPrice: 50,
          price: 30,
          vote: 0,
          brand: "",
        },
      ],
      topRated: [
        {
          image: require("@/assets/leather_gloves-400x520.jpg"),
          title: "Leather Gloves",
          oldPrice: 0,
          price: 45,
          vote: 5,
          brand: "",
        },
        {
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
          title: "Black Leather Jacket",
          oldPrice: 235,
          price: 200,
          vote: 5,
          brand: "",
        },
        {
          image: require("@/assets/spring_printed_dress.jpg"),
          title: "Spring Printed Dress",
          oldPrice: 0,
          price: 47,
          vote: 5,
          brand: "",
        },
      ],
      latestReviews: [
        {
          image: require("@/assets/black_elegant_leather_jacket.jpg"),
          title: "Black Leather Jacket",
          oldPrice: 0,
          price: 0,
          vote: 5,
          brand: "Admin",
        },
        {
          image: require("@/assets/leather_gloves-400x520.jpg"),
          title: "Leather Gloves",
          oldPrice: 0,
          price: 0,
          vote: 5,
          brand: "Beardman",
        },
        {
          image: require("@/assets/spring_printed_dress.jpg"),
          title: "Spring Printed Dress",
          oldPrice: 0,
          price: 0,
          vote: 5,
          brand: "Admin",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/style/variables.scss";
@import "@/style/global.scss";

.featured_products {
  padding: 150px 0px;

  .filter_by_gender {
    list-style: none;
    padding-left: 0;
    padding-bottom: 30px;
    margin: 0;

    li {
      background-color: #f6f6f6;
      display: inline-block;
      padding: 10px 50px;
      border: 1px solid #eaeaea;
    }
    .active {
      background-color: white;
    }
  }
  .card_container {
    display: flex;
    padding-bottom: 30px;
    .featured_products_card {
      width: calc(100% / 4);
      text-align: start;
      img {
        width: 100%;
      }
      p {
        margin-bottom: 0;
        margin-top: 15px;
        font-weight: bold;
      }
      small {
        font-size: 12px;
        display: block;
      }
      .price_cont {
        padding: 10px 0px;
        .d-price {
          padding-right: 10px;
          font-size: 12px;
          text-decoration: line-through;
          font-weight: 600;
          color: #427ed5;
        }
        .price {
          font-weight: 600;
          color: #427ed5;
        }
      }
    }
  }
}

.collection_section {
  display: flex;
  .collection_card {
    width: calc(100% / 3);
    //background-image: url("../assets/winter_collection_bg.jpg");
    background-position: top;
    position: relative;
    img {
      aspect-ratio: 1/1;
      width: 100%;
      object-fit: cover;
      object-position: top;
    }
    .card_content {
      width: 100%;
      position: absolute;
      bottom: 20%;
      left: 50%;
      transform: translateX(-50%);
      h3 {
        font-size: 40px;
        font-weight: 700;
        color: white;
      }
      small {
        display: block;
        margin: 20px 0px;
        color: white;
        font-weight: 500;
      }
      .my_light_btn {
        display: inline-block;
        margin: 0px 10px;
        font-size: 10px;
        font-weight: 600;
        padding: 10px 25px;
        border-radius: 25px;
        background-color: rgba(255, 255, 255, 0.123);
      }
    }
  }
}
.bs_section {
  padding: 150px 0px;
  .container_bs {
    position: relative;
    display: flex;
    .bs_card {
      width: calc(100% / 5);
      img {
        width: 100%;
      }
    }
    .arrow_style {
      position: absolute;

      top: 50%;
      transform: translateY(-50%);
      color: white;
      background-color: #c1c1c1;
      i {
        padding: 15px 5px;
        font-size: 10px;
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
    .offer_card {
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
        padding: 0px 50px;
        p {
          padding-right: 150px;
        }
        h1 {
          font-weight: bold;
        }
        .my_light_btn {
          display: inline-block;
          margin: 0px 10px;
          font-size: 10px;
          font-weight: 600;
          padding: 10px 25px;
          border-radius: 25px;
          background-color: rgba(255, 255, 255, 0.123);
        }
      }
    }
  }
}
.na_section {
  padding: 150px 0px;
  .container_na {
    position: relative;
    display: flex;
    .na_card {
      width: calc(100% / 5);
    }
    .arrow_style {
      position: absolute;

      top: 50%;
      transform: translateY(-50%);
      color: white;
      background-color: #c1c1c1;
      i {
        padding: 15px 5px;
        font-size: 10px;
      }
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
    gap: 25px;
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
  p {
    padding-bottom: 10px;
    color: #6b6a6b;
  }
  .logos_container {
    display: flex;
    .logo {
      width: calc(100% / 5);
    }
  }
}
</style>
