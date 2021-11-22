<template>
  <div>
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
    <div class="footer_nav_section"></div>
    <div class="pay_methods_section"></div>
  </div>
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
</style>
