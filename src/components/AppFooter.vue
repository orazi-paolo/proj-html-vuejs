<script>
import AppFooterNewsLetter from './appFooterChild/AppFooterNewsLetter.vue'
import AppFooterColList from './appFooterChild/AppFooterColList.vue'
import AppFooterCopyright from './appFooterChild/AppFooterCopyright.vue'
export default {
  data() {
    return {
      quickLinks: ['Games', 'Latest Tournament', 'Shop', 'Blog', 'Contact'],
      helpLinks: ['Faqs', 'Terms & Conditions', 'Privacy'],
      followUsLinks: ['Facebook', 'Twitter', 'Instagram', 'Youtube', 'Github'],
    }
  },
  components: {
    AppFooterNewsLetter,
    AppFooterColList,
    AppFooterCopyright
  }
}
</script>

<template>
  <footer class="bg-footer text-white">
    <AppFooterNewsLetter />
    <div class="container wow animate__animated animate__fadeInUp" data-wow-duration="1s">
      <div class="row">
        <div class="col-4">
          <a href="#">
            <img src="../assets/logo.png" alt="logo">
          </a>
          <p class="mb-5 mt-4">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum molestiae
          </p>
          <div class="social">
            <ul class="d-flex list-unstyled">
              <li class="pe-2">
                <a href="#">
                  <i class="bi bi-youtube"></i>
                </a>
              </li>
              <li class="pe-2">
                <a href="#">
                  <i class="bi bi-twitch"></i>
                </a>
              </li>
              <li class="pe-2">
                <a href="#">
                  <i class="bi bi-facebook"></i>
                </a>
              </li>
              <li class="pe-2">
                <a href="#">
                  <i class="bi bi-instagram"></i>
                </a>
              </li>
            </ul>
          </div>
        </div>
        <AppFooterColList title="Quick Links" :items="quickLinks" class="wow animate__animated animate__fadeInUp"
          data-wow-duration="1s" />
        <AppFooterColList title="Help" :items="helpLinks" class="wow animate__animated animate__fadeInUp"
          data-wow-duration="1s" />
        <AppFooterColList title="Follow Us" :items="followUsLinks" class="wow animate__animated animate__fadeInUp"
          data-wow-duration="1s" />
        <div class="col-2">
          <h5>Contacts</h5>
          <p><span>Location:</span> <br> 4 Mayfield, Buckden, PE19 5SZ</p>
          <p><span>Phones:</span> <br> (302) 555-0107</p>
        </div>
      </div>
    </div>
    <AppFooterCopyright class="wow animate__animated animate__fadeInUp" data-wow-duration="1s" />
  </footer>

</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

.bg-footer {
  background-color: #27344a;
}

ul li a {
  color: lightgray;
  border: 1px solid gray;
  border-radius: 50%;
  padding: $padding-md;
  transition: background-color 0.3s, border-color 0.3s;

  &:hover {
    border-color: $lightOliveGreen;
    background-color: $lightOliveGreen;
  }
}

span {
  color: $lightOliveGreen;
}

.container {
  padding-bottom: 150px;
}
</style>