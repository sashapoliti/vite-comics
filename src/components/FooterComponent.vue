<template>
  <footer>
    <div id="top-footer">
      <div class="container">top footer</div>
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
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data() {
    return {
      dcComics: [
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
          name: "TV",
          url: "#",
        },
        {
          name: "Games",
          url: "#",
        },
        {
          name: "Videos",
          url: "#",
        },
        {
          name: "News",
          url: "#",
        },
      ],
      shop: [
        {
          name: "Shop DC",
          url: "#",
        },
        {
          name: "Shop DC Collectibles",
          url: "#",
        },
      ],
      dc: [
        {
          name: "Term Of Use",
          url: "#",
        },
        {
          name: "Privacy policy (New)",
          url: "#",
        },
        {
          name: "Ad Choices",
          url: "#",
        },
        {
          name: "Advertising",
          url: "#",
        },
        {
          name: "Jobs",
          url: "#",
        },
        {
          name: "Subscriptions",
          url: "#",
        },
        {
          name: "Talent Workshops",
          url: "#",
        },
        {
          name: "CPSC Certificates",
          url: "#",
        },
        {
          name: "Ratings",
          url: "#",
        },
        {
          name: "Shop Help",
          url: "#",
        },
        {
          name: "Contact Us",
          url: "#",
        },
      ],
      sites: [
        {
          name: "DC",
          url: "#",
        },
        {
          name: "MAD Magazine",
          url: "#",
        },
        {
          name: "DC Kids",
          url: "#",
        },
        {
          name: "DC Universe",
          url: "#",
        },
        {
          name: "DC Power Visa",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

footer {
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
    }
  }
}
</style>
