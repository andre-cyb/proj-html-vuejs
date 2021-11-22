<template>
  <div class="my-cont">
    <section class="featured_products">
      <!-- da creare un componente -->
      <div class="title_section">
        <hr />
        <div class="title"><h3>Featured Products</h3></div>
        <hr />
        <p>Must have products from our top sellers</p>
      </div>
      <!-- ---------------------- -->
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
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {},
};
</script>

<style lang="scss">
.my-cont {
  max-width: 1140px;
  margin: auto;
  .featured_products {
    padding: 30px;
    .title_section {
      width: 100%;

      .title {
        display: inline-block;
        width: 30%;
      }
      hr {
        display: inline-block;
        height: 2px;
        width: 35%;
        background-color: rgb(44, 44, 44);
        vertical-align: center;
      }
      p {
        padding-bottom: 30px;
      }
    }
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
    .featured_products_card {
      width: calc(100% / 4);
      img {
        width: 100%;
      }
    }
  }
}
</style>
