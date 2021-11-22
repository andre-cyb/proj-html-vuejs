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
        <div class="col-3">
          <img
            src="@/assets/classic_shop_logo_footer.png"
            width="100%"
            alt=""
          />
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum
            nihil maiores rem assumenda saepe fugiat, vel voluptatum ad itaque
            neque in reprehenderit quia eligendi? Molestias ex dolorum sit
            repellendus praesentium.
          </p>
          <ul>
            <li><i class="fa fa-facebook" aria-hidden="true"></i></li>
            <li><i class="fa fa-twitter" aria-hidden="true"></i></li>
            <li><i class="fa fa-instagram" aria-hidden="true"></i></li>
            <li><i class="fa fa-youtube-play" aria-hidden="true"></i></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="pay_methods_section"></div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {},
};
</script>

<style lang="scss">
.subscribe_section {
  background-color: #64686c;
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
    ul {
      list-style: none;
      margin: 0%;
      padding: 0;
      li {
        display: inline;
        i {
          padding-right: 20px;
        }
      }
    }
  }
}
</style>
