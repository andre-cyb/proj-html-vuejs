<template>
  <div class="col-3 my_preview">
    <p>{{ title }}</p>
    <ul>
      <li>
        <div class="item_details">
          <small>Black Jacket</small>
          <span class="fw-bold">$125</span>
        </div>
        <div class="item_image">
          <img src="../assets/black_leather_jacket.jpg" width="100%" alt="" />
        </div>
      </li>
      <li>
        <div class="item_details">
          <small>Black Jacket</small>
          <span class="fw-bold">$125</span>
        </div>
        <div class="item_image">
          <img src="../assets/black_leather_jacket.jpg" width="100%" alt="" />
        </div>
      </li>
      <li>
        <div class="item_details">
          <small>Black Jacket</small>
          <span class="fw-bold">$125</span>
        </div>
        <div class="item_image">
          <img src="../assets/black_leather_jacket.jpg" width="100%" alt="" />
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PreviewItem",
  props: ["title"],
};
</script>

<style lang="scss">
.my_preview {
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
</style>
