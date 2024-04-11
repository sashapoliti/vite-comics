<template>
  <a :href="url">
    <div class="cover">
      <img :src="thumb" :alt="`Copertina di ${series}`" />
    </div>
    <h6 class="text-uppercase">{{ series }}</h6>
  </a>
</template>

<script>
export default {
  name: "MainComicsCard",
  props: {
    series : String,
    thumb : String,
    price : String,
    type  : String,
    url: {
      type: String,
      default: "#", // Imposta '#' come valore predefinito per la prop "url"
    },
  },
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
  h6 {
    margin-top: 15px;
    font-size: 0.9rem;
    font-weight: 400;
  }
}
</style>
