<template>
  <main>
    <div id="jumbotron"></div>
    <div class="container">
      <h2 class="text-uppercase">Current Series</h2>
      <div class="comics container">
        <div class="row gx-4 gy-5">
          <div class="col-12 col-md-6 col-lg-4 col-xxl-2" v-for="(item, index) in comics" :key="index">
            <MainComicsCard
            :series="item.series"
            :thumb="item.thumb"
            :price="item.price"
            :type="item.type" />
          </div>
        </div>
      </div>
      <div class="text-center">
        <button class="text-uppercase">Load More</button>
      </div>
    </div>
  </main>
</template>

<script>
import {comics} from '../data/storage.js';
import MainComicsCard from './MainComicsCard.vue';
export default {
  name: "MainComponent",
  components: {
    MainComicsCard
  },
  data() {
    return {
      comics
    }
  }
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

main {
  background-color: $main-bg;
  color: $general-white;
  div#jumbotron {
    width: 100%;
    height: 400px;
    background-image: url('/images/jumbotron.jpg');
  }
  div.container {
    h2 {
      display: inline-block;
      font-family: $anton;
      background-color: $general-blue;
      padding: 10px 35px;
      transform: translateY(-50%);
    }
    div.comics {
      margin-top: -10px;
      padding-bottom: 30px;
    }
    button {
      font-family: $anton;
      font-size: 0.9rem;
      background-color: $general-blue;
      color: $general-white;
      padding: 20px 70px;
      margin-bottom: 20px;
      border: 0;
      line-height: 0;
      &:hover {
        filter: brightness(108%);
        transition-duration: 0.3s;
      }
    }
  }
}
</style>
