<template>
  <div class="offer_card text-white">
    <img :src="image" width="100%" alt="" />
    <div class="offer_card_content">
      <h2>{{ offer }}</h2>
      <p>{{ text }}</p>
      <button>VIEW MORE</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "BannerOffer",
  props: ["offer", "text", "image"],
};
</script>

<style lang="scss">
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
    padding-left: 50px;
  }
}
</style>
