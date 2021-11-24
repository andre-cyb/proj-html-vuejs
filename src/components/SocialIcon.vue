<template>
  <ul class="icon_list">
    <li><i class="fa fa-facebook" aria-hidden="true"></i></li>
    <li><i class="fa fa-twitter" aria-hidden="true"></i></li>
    <li><i class="fa fa-instagram" aria-hidden="true"></i></li>
    <li><i class="fa fa-youtube-play" aria-hidden="true"></i></li>
  </ul>
</template>
<script>
export default {
  name: "SocialIcon",
  components: {},
};
</script>
<style lang="scss">
.icon_list {
  list-style: none;
  margin: 0;
  padding: 0;
  li {
    display: inline;
    i {
      padding-right: 20px;
    }
  }
}
</style>
