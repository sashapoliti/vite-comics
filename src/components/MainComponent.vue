<template>
  <main>
    <div id="jumbotron"></div>
    <div class="container">
      <h2 class="text-uppercase">Current Series</h2>
    </div>
  </main>
</template>

<script>
export default {
  name: "MainComponent"
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

main {
  font-family: $anton;
  background-color: $main-bg;
  color: $general-white;
  div#jumbotron {
    width: 100%;
    height: 400px;
    background-image: url('/images/jumbotron.jpg');
  }
  div.container {
    height: 120px;
    h2 {
      display: inline-block;
      background-color: $general-blue;
      padding: 10px 35px;
      transform: translateY(-50%);
    }
  }
}
</style>
