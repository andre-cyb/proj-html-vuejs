<template>
  <footer>
    <div class="subscribe_section">
      <div class="form_cont">
        <div class="text_style">
          <i class="fa fa-envelope-o" aria-hidden="true"></i>
          <h4>Subscribe now and get special offers</h4>
        </div>
        <div class="form_style">
          <form action="">
            <input type="email" />
            <button>SEND</button>
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
            Email:info@company.com<br />
            Web: Theme-fusion.com<br />
          </p>
          <SocialIcon></SocialIcon>
        </div>
        <PreviewItem title="TOP RATED PRODUCTS"></PreviewItem>
        <!-- COLONNA FOOTER TOP PRODUCTS -->
        <div class="col-3 my_recent_post">
          <!-- COLONNA FOOTER RECENT POSTS -->
          <p>RECENT POSTS</p>
          <ul>
            <li v-for="(post, i) in recentPosts" :key="`post` + i">
              <i class="fa fa-chevron-right" aria-hidden="true"></i>
              <p class="ps-2">{{ post.post }}</p>
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
.subscribe_section {
  background-color: #303337;
  padding: 70px 0px;
  display: flex;
  justify-content: center;
  .form_cont {
    width: 1140px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    .text_style {
      i {
        font-size: 30px;
        color: #6b6a6b;
      }
      h4 {
        display: inline-block;
        padding-left: 30px;
        color: white;
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
      ul {
        list-style: none;
        margin: 0;
        padding: 0;
        li {
          padding: 10px 0px;
          display: flex;
          border-bottom: 1px solid #303337;
          i {
            font-size: 10px;
            line-height: 25px;
          }

          p {
            display: inline;
            margin: 0;
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
          border: 1px solid #303337;
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
    list-style: none;
    margin: 0%;
    padding: 0;
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
