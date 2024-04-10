<template>
  <header>
    <div class="container d-flex justify-content-between align-items-center">
      <div id="logo">
        <img class="img-fluid" src="/images/dc-logo.png" alt="Logo" />
      </div>
      <ul class="d-flex">
        <li v-for="(item, index) in menu" :key="index">
          <a class="d-flex align-items-center text-uppercase" :href="item.url">
            {{ item.name }}
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      menu: [
        {
          name: "Characters",
          url: "#",
        },
        {
          name: "Comics",
          url: "#",
        },
        {
          name: "Movies",
          url: "#",
        },
        {
          name: "Tv",
          url: "#",
        },
        {
          name: "Games",
          url: "#",
        },
        {
          name: "Collectibles",
          url: "#",
        },
        {
          name: "Videos",
          url: "#",
        },
        {
          name: "Fans",
          url: "#",
        },
        {
          name: "News",
          url: "#",
        },
        {
          name: "Shop",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

header {
  font-family: $anton;
  font-size: 0.9rem;
  & > div {
    height: 120px;
    div#logo {
      width: 80px;
      aspect-ratio: 1 / 1;
    }
    ul {
      li {
        &:last-child {
          a {
            margin-right: 0;
          }
        }
        a {
          height: 120px;
          margin-right: 40px;
          position: relative;
          &:hover {
            color: $general-blue;
            transition-duration: 0.3s;
            &::after {
              content: "";
              position: absolute;
              left: 0;
              bottom: 0;
              width: 100%;
              height: 5px;
              background-color: $general-blue;
            }
          }
        }
      }
    }
  }
}
</style>
