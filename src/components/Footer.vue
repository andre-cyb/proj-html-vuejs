<template>
  <footer>
    <div class="subscribe_section">
      <div class="form_cont">
        <div class="icon_style">
          <i class="fa fa-envelope-o" aria-hidden="true"></i>
        </div>
        <div class="text_style">
          <h4>Subscribe now and get special offers</h4>
        </div>
        <div class="form_style">
          <form action="">
            <input type="email" placeholder="insert your email" />
            <button type="button" class="btn my_btn">SEND</button>
          </form>
        </div>
      </div>
    </div>
    <div class="footer_nav_section">
      <div class="menu_cont row">
        <div class="col-3 my_col">
          <!-- COLONNA FOOTER INFO AVADA -->
          <img src="@/assets/classic_shop_logo_footer.png" width="70%" alt="" />
          <p>
            12345 North Main Sreet,<br />
            New York, NY 555555<br />
            Phone: 1.800.5555.6789<br />
            Email: info@company.com<br />
            Web: Theme-fusion.com<br />
          </p>
          <SocialIcon></SocialIcon>
        </div>
        <PreviewItem title="TOP RATED PRODUCTS" :Arr="topRated"></PreviewItem>
        <!-- COLONNA FOOTER TOP PRODUCTS -->
        <div class="col-3 my_recent_post">
          <!-- COLONNA FOOTER RECENT POSTS -->
          <p>RECENT POSTS</p>
          <ul class="ps-0">
            <li v-for="(post, i) in recentPosts" :key="`post` + i">
              <i class="fa fa-chevron-right" aria-hidden="true"></i>
              <p class="ps-2">
                <a href="#">{{ post.post }}</a>
              </p>
            </li>
          </ul>
        </div>
        <div class="col-3 my_tags">
          <!-- COLONNA FOOTER TAG -->
          <p>TAGS</p>
          <ul class="tags_list">
            <li class="d-inline" v-for="(tag, i) in tags" :key="`tag` + i">
              <a class="tag_link" :href="`/` + tag.name">{{ tag.name }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="pay_methods_section">
      <ul>
        <li>Copyright 2012-2020</li>
        <span class="text-white">|</span>
        <li>Avada Theme Fusion</li>
        <span class="text-white">|</span>
        <li>All Right Reserved</li>
        <span class="text-white">|</span>
        <li class="border_left">Powered By Wordpress</li>
      </ul>
      <img src="../assets/payment_cards_footer.png" alt="" />
    </div>
  </footer>
</template>

<script>
import PreviewItem from "./PreviewItem.vue";
import SocialIcon from "./SocialIcon.vue";
export default {
  components: { PreviewItem, SocialIcon },
  name: "Footer",
  props: {},
  data() {
    return {
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
      recentPosts: [
        {
          post: "at aptent vehicula blandit  ",
        },
        {
          post: "aliquet purus dui elementum ",
        },
        {
          post: "Leo duis parturient tempor ",
        },
        {
          post: "class penatibus fames cursus ",
        },
        {
          post: "sagittis ante primis dis",
        },
        {
          post: "Id lacinia neque vulputate ",
        },
      ],
      tags: [
        {
          name: "Black",
        },
        {
          name: "boots",
        },
        {
          name: "Brown",
        },
        {
          name: "Casual",
        },
        {
          name: "D&G",
        },
        {
          name: "Fabric",
        },
        {
          name: "flower",
        },
        {
          name: "Grey",
        },
        {
          name: "hat",
        },
        {
          name: "Hipster",
        },
        {
          name: "lines",
        },
        {
          name: "multi-purpose",
        },
        {
          name: "New-York",
        },
        {
          name: "Outdoors",
        },
        {
          name: "red",
        },
        {
          name: "responsive",
        },
        {
          name: "summer",
        },
        {
          name: "sweater",
        },
        {
          name: "Travel",
        },
        {
          name: "Warm",
        },
        {
          name: "white",
        },
        {
          name: "winter",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/style/variables.scss";
@import "@/style/global.scss";
.subscribe_section {
  background-color: #303337;
  padding: 70px 0px;
  display: flex;
  justify-content: center;
  .form_cont {
    width: 1140px;
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .icon_style {
      background-color: #2b2e32;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      position: relative;
      i {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -55%);
        font-size: 30px;
        color: #6b6a6b;
      }
    }
    .text_style {
      margin-right: auto;
      h4 {
        display: inline-block;
        padding-left: 30px;
        font-weight: 700;
        color: white;
      }
    }
    .form_style {
      .my_btn {
        color: white;
        background-color: $primary_color;
        border-radius: 20px;
        margin: 0px 15px;
        padding: 6px 16px;
        font-weight: 700;
        font-size: 13px;
        &:hover {
          box-shadow: 1px 2px 10px $primary_color;
        }
      }
      input {
        border: none;
        border-radius: 20px;
        width: 250px;
        height: 34px;
        padding: 0px 10px;
      }
    }
  }
}
.footer_nav_section {
  padding: 70px 0px;
  background-color: #2b2e32;
  color: white;
  .menu_cont {
    width: 1140px;

    margin: auto;
    text-align: start;
    .my_col {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .my_recent_post {
      text-align: start;

      li {
        padding: 10px 0px;
        display: flex;
        border-bottom: 1px solid #35383c;
        i {
          font-size: 10px;
          line-height: 25px;
        }

        p {
          display: inline;
          margin: 0;
          a {
            text-decoration: none;
            color: white;
          }
        }
      }
    }
    .my_tags {
      .tags_list {
        margin: 0%;
        padding: 0;
        display: flex;
        flex-wrap: wrap;
        li {
          margin: 1px;
          border: 1px solid #35383c;
          .tag_link {
            padding: 10px;
            text-decoration: none;
            color: white;
          }
        }
      }
    }
  }
}
.pay_methods_section {
  background-color: #1d1f22;
  ul {
    padding-top: 20px;
    li {
      color: white;
      font-size: 13px;
      padding: 10px;
      display: inline-block;
    }
  }
  img {
    padding: 10px 0px;
  }
}
</style>
