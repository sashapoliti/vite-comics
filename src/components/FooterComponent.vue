<template>
  <footer>
    <div id="top-footer">
      <div class="container d-flex justify-content-between align-items-center">
        <FooterShopCards
          v-for="(item, index) in shopCards"
          :key="index"
          :title="item.title"
          :image="item.img"
          :url="item.url"
        />
      </div>
    </div>
    <div id="middle-footer">
      <div class="container">
        <div class="row">
          <div class="col-1">
            <ul>
              <h5 class="text-uppercase">Dc comics</h5>
              <li v-for="(item, index) in dcComics" :key="index">
                <a href="item.url">{{ item.name }}</a>
              </li>
            </ul>
            <ul>
              <h5 class="text-uppercase">Shop</h5>
              <li v-for="(item, index) in shop" :key="index">
                <a href="item.url">{{ item.name }}</a>
              </li>
            </ul>
          </div>
          <div class="col-1">
            <ul>
              <h5 class="text-uppercase">Dc</h5>
              <li v-for="(item, index) in dc" :key="index">
                <a href="item.url">{{ item.name }}</a>
              </li>
            </ul>
          </div>
          <div class="col-1">
            <ul>
              <h5 class="text-uppercase">sites</h5>
              <li v-for="(item, index) in sites" :key="index">
                <a href="item.url">{{ item.name }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div id="bottom-footer">
      <div class="container d-flex justify-content-between align-items-center">
        <a id="call-to-action" class="text-uppercase" href="#">Sign-up now!</a>
        <div class="social-icons d-flex align-items-center">
          <span class="text-uppercase">follow us</span>
          <div class="icon" v-for="(item, index) in socialIcons" :key="index">
            <a href="item.url">
              <img
                :src="`/images/${item.img}`"
                :alt="`Icona di ${item.name}`"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import {dcComics, shop, dc, sites, socialIcons, shopCards} from '../data/storage.js';
import FooterShopCards from "./FooterShopCards.vue";
export default {
  name: "FooterComponent",
  components: {
    FooterShopCards,
  },
  data() {
    return {
      dcComics,
      shop,
      dc,
      sites,
      socialIcons,
      shopCards,
    };
  },
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

footer {
  #top-footer {
    background-color: $general-blue;
    color: $general-white;
    div.container {
      padding-top: 30px;
      padding-bottom: 30px;
    }
  }
  #middle-footer {
    background-image: url("/images/footer-bg.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    div.container {
      padding-top: 50px;
      padding-bottom: 50px;
      background-image: url("/images/dc-logo-bg.png");
      background-repeat: no-repeat;
      background-position: right 1.5% bottom 50%;
      div.col-1 {
        width: 150px;
        &:first-child {
          ul {
            &:first-child {
              padding-bottom: 20px;
            }
          }
        }
        ul {
          padding: 0;
          h5 {
            font-family: $anton;
            color: $general-white;
          }
          li {
            height: 21px;
            a {
              color: $footer-text;
              font-size: 0.8rem;
              &:hover {
                text-decoration: underline;
              }
            }
          }
        }
      }
    }
  }
  #bottom-footer {
    background-color: $footer-bg;
    div.container {
      height: 120px;
      #call-to-action {
        color: $general-white;
        padding: 10px 15px;
        font-size: 1rem;
        font-weight: 600;
        border: 2px solid $general-blue;
        &:hover {
          background-color: $general-blue;
          transition-duration: 0.3s;
        }
      }
      div.social-icons {
        span {
          font-family: $anton;
          font-size: 1.4rem;
          margin-right: 10px;
          color: $general-blue;
        }
        div.icon {
          margin-left: 20px;
          a {
            &:hover {
              img {
                filter: brightness(200%);
                transition-duration: 0.6s;
              }
            }
          }
        }
      }
    }
  }
}
</style>
