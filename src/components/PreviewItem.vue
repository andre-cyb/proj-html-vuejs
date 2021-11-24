<template>
  <div class="col-3 my_preview">
    <p>{{ title }}</p>
    <ul>
      <li v-for="(product, i) in Arr" :key="`product` + i">
        <div class="item_details">
          <p class="item_title">{{ product.title }}</p>
          <div v-if="product.vote !== 0">
            <i
              class="fa fa-star"
              aria-hidden="true"
              v-for="(star, i) in product.vote"
              :key="`star` + i"
            ></i>
          </div>
          <span v-if="product.oldPrice !== 0" class="oldPrice"
            >${{ product.oldPrice }}</span
          >
          <span v-if="product.price !== 0" class="price"
            >${{ product.price }}</span
          >
          <div class="brand" v-if="product.brand !== ``">
            by {{ product.brand }}
          </div>
        </div>
        <div class="item_image">
          <img :src="product.image" width="100%" alt="" />
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PreviewItem",
  props: {
    Arr: Array,
    title: String,
  },
};
</script>

<style lang="scss">
@import "@/style/variables.scss";
.my_preview {
  text-align: start;
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
    li {
      padding: 10px 0px;
      display: flex;
      border-bottom: 1px solid #eaeaea;
      i {
        padding-right: 1px;
        font-size: 13px;
      }
      .item_details {
        width: 80%;
        .item_title {
          margin-bottom: 0;
          font-size: 13px;
        }
        i {
          color: $primary_color;
        }
        .oldPrice {
          font-weight: 700;
          padding-right: 5px;
          font-size: 12px;
          text-decoration: line-through;
          font-weight: 600;
        }
        .price {
          font-weight: bold;
          font-size: 14px;
        }
        .brand {
          font-size: 13px;
        }
      }
      .item_image {
        width: 20%;
      }
    }
  }
}
</style>
