<script>
import BaseButton from "../baseComponents/BaseButton.vue"
export default {
  data() {
    return {
      scroll: false,
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
    }
  },
  components: {
    BaseButton
  },
  methods: {
    isPageScrolled() {
      this.scroll = true
    },

  },
  mounted() {
    document.addEventListener('scroll', this.isPageScrolled)
  }
}
</script>

<template>
  <section id="header-nav">
    <nav class="navbar navbar-expand-lg" :class="scroll ? 'nav-fixed' : ''">
      <div class="container">
        <a class="navbar-brand" href="#">
          <img src="../../assets/logo.png" alt="Logo Futio" class="d-inline-block align-text-top">
        </a>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav">
            <li v-for="nav in navLink" class="link">
              <a class="nav-link" href="#">{{ nav.name }}</a>
              <div class="internal-link" v-if="nav.internal">
                <ul>
                  <li v-for="int in nav.internal" class="int"><a class="nav-link" href="#">{{ int.intLink }}</a>
                    <div class="sub-link" v-if="int.sub">
                      <ul class="sub">
                        <li v-for="sub in int.sub"><a class="nav-link" href="#">{{ sub.subLink }}</a></li>
                      </ul>
                    </div>
                  </li>
                </ul>
              </div>
            </li>
          </ul>
          <div class="d-flex align-items-center">
            <div class="cart p-2 me-2 position-relative"><img src="../../assets/icon/cart-icon.png" alt="cart"><span
                class="number-object-cart">03</span></div>
            <BaseButton contentButton="LIVE STREAMING" :isArrow="false" />
          </div>
        </div>
      </div>
    </nav>
  </section>
</template>

<style lang="scss" scoped>
#header-nav .navbar-nav {
  margin-right: 80px;
}

.link:hover>.internal-link {
  display: block;
}

.int:hover .sub-link {
  display: block;
}

.internal-link,
.sub-link {
  display: none;

  ul {
    list-style-type: none;
  }
}

a {
  color: white;
  font-family: "Orbitron", sans-serif;

  &:hover,
  li .active {
    color: #94CB53
  }
}

#header-nav .nav-fixed {
  background-color: #30405F;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 1;
}

.collapse {
  justify-content: flex-end;

  .cart {
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
</style>