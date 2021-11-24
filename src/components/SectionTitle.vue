<template>
  <div class="title_section">
    <div class="d-flex">
      <hr />
      <div class="title">
        <h3>{{ title }}</h3>
      </div>
      <hr />
    </div>
    <p>{{ subtitle }}</p>
  </div>
</template>

<script>
export default {
  name: "SectionTitle",
  props: ["title", "subtitle"],
};
</script>

<style lang="scss">
.title_section {
  width: 100%;

  .title {
    display: inline-block;
    width: 22%;
    h3 {
      font-weight: 700;
    }
  }
  hr {
    display: inline-block;
    height: 2px;
    width: 39%;
    background-color: rgb(44, 44, 44);
    vertical-align: center;
  }
  p {
    padding-bottom: 30px;
  }
}
</style>
