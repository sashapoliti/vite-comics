<template>
  <a class="d-flex justify-content-center align-items-center" href="#">
    <div class="icon d-flex justify-content-center align-items-center">
      <img
        class="img-fluid h-100 "
        :src="`/images/${image}`"
        alt=""
      />
    </div>
    <span class="text-uppercase">{{ title }}</span>
  </a>
</template>

<script>
export default {
  name: "FooterShopCards",
  props: ['title', 'image']
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

a {
  padding: 20px 34px;
  border: 2px solid rgba(255, 255, 255, 0);
  &:hover {
    border-color: $general-white;
    transition-duration: 0.4s;
  }
  div.icon {
    height: 60px;
    aspect-ratio: 1 / 1;
  }
  span {
    font-size: 0.9rem;
    margin-left: 10px;
  }
}
</style>
