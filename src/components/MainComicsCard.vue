<template>
  <a href="#">
    <div class="cover">
      <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="" />
    </div>
    <h6 class="text-uppercase">blblabla</h6>
  </a>
</template>

<script>
export default {
  name: "MainComicsCard",
  props: ["series", "thumb", "price", "type", "url"],
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

a {
  .cover {
    width: 100%;
    aspect-ratio: 1 / 1;
    overflow: hidden;
    img {
      width: 100%;
    }
  }
}
</style>
