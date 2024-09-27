<script>
// import components
import BaseButton from "../baseComponents/BaseButton.vue"

export default {
  data() {
    return {
      scroll: false,
      showCart: false,
      active: 0,
      cartNumber: "0",
      navLink: [
        {
          name: "Home",
        },
        {
          name: "Games",
          internal: [{ intLink: "Games" }, { intLink: "Games Details" }, { intLink: "Match Details" }]
        },
        {
          name: "Shop",
          internal: [{ intLink: "Shop" }, { intLink: "Shop Single" }, { intLink: "Shop Single 2" }, { intLink: "Shop Single 3" }, { intLink: "Shop Single 4" }]
        },
        {
          name: "Pages",
          internal: [{ intLink: "About Us" }, { intLink: "Team", sub: [{ subLink: "All Team" }, { subLink: "Team Details" }] }, { intLink: "Player", sub: [{ subLink: "Player" }, { subLink: "Player Single" }] }, { intLink: "Upcoming Matches" }, { intLink: "FAQs" }, { intLink: "Privacy Policy" }, { intLink: "Terms" }, { intLink: "Coming Soon" }, { intLink: "Error" }]
        },
        {
          name: "Blog",
          internal: [{ intLink: "Blog" }, { intLink: "Blog Single" }]
        },
        {
          name: "Contact",
        }
      ],
      cartObject: [
        { name: "Havit RGB Headphones", urlImage: "shop-image-3.png", salePrice: "380.00", price: "410.00" },
        { name: "Touch Controller Grip", urlImage: "shop-image-5.png", salePrice: "380.00", price: "410.00" },
        { name: "Gaming Microphones", urlImage: "shop-image-8.png", salePrice: "380.00", price: "410.00" },
      ]
    }
  },
  components: {
    BaseButton
  },
  methods: {
    isPageScrolled() {
      this.scroll = true
    },
    isActive(i) {
      this.active = i
    },
    getCartImageUrl(url) {
      return new URL(`../../assets/${url}`, import.meta.url).href;
    },
    deleteItemCart(i) {
      this.cartObject.splice(i, 1)
    },
    isShowCart() {
      this.showCart = !this.showCart
    }

  },
  mounted() {
    window.addEventListener('scroll', this.isPageScrolled)
  },
  computed: {
    cartLength() {
      this.cartObject.length < 10 ? this.cartNumber = '0' + this.cartObject.length : this.cartNumber = this.cartObject.length;
    }
  }
}
</script>

<template>
  <!--Header navbar-->
  <section id="header-nav">
    <nav class="navbar navbar-expand-lg" :class="scroll ? 'nav-fixed' : ''">
      <div class="container">
        <!--Logo-->
        <a class="navbar-brand" href="#">
          <img src="../../assets/logo.png" alt="Logo Futio" class="d-inline-block align-text-top">
        </a>
        <div class="collapse navbar-collapse">
          <!--Main Links-->
          <ul class="navbar-nav">
            <li v-for="(nav, index) in navLink" class="link" @click="isActive(index)">
              <a href="#" :class="(active === index) ? 'active' : ''">{{ nav.name }} <span v-if="nav.internal"
                  class="arrow"><img src="../../assets/svg/c-down-arrow.svg" alt=""></span></a>
              <div class="internal-link" v-if="nav.internal">
                <ul>
                  <li v-for="int in nav.internal" class="int"><a href="#">{{ int.intLink }} <span v-if="int.sub"><img
                          src="../../assets/svg/b-right-arrow.svg" alt=""></span></a>
                    <div class="sub-link" v-if="int.sub">
                      <ul class="sub">
                        <li v-for="sub in int.sub"><a href="#">{{ sub.subLink }}</a></li>
                      </ul>
                    </div>
                  </li>
                </ul>
              </div>
            </li>
          </ul>
          <!--Cart and Button-->
          <div class="d-flex align-items-center">
            <div class="cart position-relative p-2 me-2">
              <div @click="isShowCart()">
                <img src="../../assets/icon/cart-icon.png" alt="cart">
                <!--Number of Items in the cart-->
                <p class="number-object-cart" v-bind="cartLength" v-if="cartObject.length">
                  {{ cartNumber }}
                </p>
              </div>
              <!--Items in Cart-->
              <div class="visual-cart" :class="showCart ? 'active' : ''" v-if="cartObject.length">
                <div class="info-cart px-4 d-flex justify-content-between">
                  <h3>Cart</h3>
                  <p>{{ cartNumber }}</p>
                </div>
                <!--card of single item in the cart-->
                <ul>
                  <li v-for="(cartItem, index) in cartObject" class="px-4 py-1 m-0">
                    <div class="card mb-3">
                      <span class="fw-bold delete-item" @click="deleteItemCart(index)">X</span>
                      <div class="row g-0">
                        <div class="col-md-4 my-auto ps-2">
                          <!--Image of the item-->
                          <img :src="getCartImageUrl(cartItem.urlImage)" class="img-fluid rounded-start"
                            :alt="cartItem.name">
                        </div>
                        <!--body of the card-->
                        <div class="col-md-8">
                          <div class="card-body">
                            <h5 class="card-title">{{ cartItem.name }}</h5>
                            <span class="sale">${{ cartItem.salePrice }}</span> <del>${{ cartItem.price }}</del>
                          </div>
                        </div>
                      </div>
                    </div>
                  </li>
                </ul>
                <!--checkout button-->
                <div class="checkout-button text-center">
                  <BaseButton contentButton="CHECKOUT" :isArrow="false" />
                </div>
              </div>
            </div>
            <!--button of live streaming-->
            <BaseButton contentButton="LIVE STREAMING" :isArrow="false" />
          </div>
        </div>
      </div>
    </nav>
  </section>
</template>

<style lang="scss" scoped>
ul {
  font-size: 18px;
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.cart .active {
  transform: translateY(-150px);
  visibility: visible;
  opacity: 1;
}

.visual-cart {
  padding: 10px 0;
  width: 350px;
  position: absolute;
  right: 0;
  top: 550%;
  transform: translateY(0px);
  transition: 0.4s;
  visibility: hidden;
  opacity: 0;
  border-radius: 5px;

  &,
  .card {
    color: white;
    background-color: #30405F;
  }

  .sale {
    color: #94CB53
  }
}


li {
  position: relative;
  margin-right: 15px;
}

#header-nav .navbar-nav {
  margin-right: 80px;
}

.link:hover>.internal-link {
  display: block;
  position: absolute;
  left: -50%;
  top: 100%;
}

.int:hover .sub-link {
  display: block;
  position: absolute;
  left: 98%;
  top: 10%;
}

.internal-link,
.sub-link {
  display: none;
  background-color: #30405F;
  padding-left: 40px;
  border-radius: 3px;
  width: 220px;
  box-shadow: 0 0 3px black;
  z-index: 2;

  li {
    margin: 15px 0;
  }
}

li a {
  color: white;
  font-family: "Orbitron", sans-serif;
  font-weight: bold;

  &:hover {
    color: #94CB53;
    transition: 0.3s;

    img {
      filter: invert(77%) sepia(18%) saturate(1178%) hue-rotate(44deg) brightness(94%) contrast(89%);
    }
  }
}



.delete-item {
  display: none;
  position: absolute;
  right: 0;
  top: -10px;
}

.card:hover .delete-item {
  display: inline;
  color: #94CB53;
}

li .active {
  color: #94CB53
}


#header-nav {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1;
}

#header-nav .nav-fixed {
  background-color: #30405F;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 10;
}

.collapse {
  justify-content: flex-end;

  li a {
    text-decoration: none;
  }

  .cart {
    position: relative;
    cursor: pointer;

    .number-object-cart {
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 500;
      background-color: #08CB7B;
      width: 20px;
      height: 20px;
      border-radius: 100%;
      position: absolute;
      top: 0;
      right: 2px;
    }
  }
}

@media (max-width: 1200px) {
  .navbar-expand-lg .navbar-collapse {
    display: flex !important;
    gap: 40px;
    justify-content: center;
    gap: 20px;
    flex-basis: auto;

    .arrow {
      display: none;
    }

    .navbar-nav {
      flex-direction: row;
    }

    a {
      font-size: 16px;
    }
  }
}

@media (max-width: 992px) {
  .container {
    flex-direction: column;
    gap: 20px;
  }

  .int:hover .sub-link {
    left: -120%;
    top: 10%;
  }

  #header-nav .navbar-nav {
    margin: 0;
  }

  .visual-cart {
    left: -100%;
  }

  .navbar-expand-lg .navbar-collapse {
    display: flex !important;
    flex-direction: column;
    justify-content: center;
    flex-basis: auto;

    a {
      font-size: 16px;
    }

    .soldier {
      display: none;
    }
  }
}

@media (max-width: 576px) {

  .navbar-expand-lg .navbar-collapse {
    flex-basis: auto;
    font-size: 16px;
  }
}


.collapse:not(.show) {
  display: block;
}
</style>