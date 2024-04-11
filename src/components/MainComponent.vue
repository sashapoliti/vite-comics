<template>
  <main>
    <div id="jumbotron"></div>
    <div class="container">
      <h2 class="text-uppercase">Current Series</h2>
      <div class="comics container">
        <div class="row">
          <div class="col-2">
            <MainComicsCard />
          </div>
        </div>
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
    }
  }
}
</style>
