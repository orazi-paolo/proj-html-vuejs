<script>
import BaseSectionTitle from '../baseComponents/BaseSectionTitle.vue';
import BaseButton from '../baseComponents/BaseButton.vue';
import PlayButton from '../baseComponents/PlayButton.vue';

export default {
  data() {
    return {

    }
  }, components: {
    BaseSectionTitle,
    BaseButton,
    PlayButton
  }
}
</script>

<template>
  <!--Section Jumbotron-->
  <section id="jumbotron" class="wow animate__animated animate__fadeInUp position-relative h-100"
    data-wow-duration="1s"
    data-wow-delay="1s">
    <img src="../../assets/game-controler.png" class="position-absolute controller" alt="">
    <div class="container h-100">
      <div class="row h-100">
        <!--Title Section-->
        <div class="col-6 title">
          <BaseSectionTitle contentGreen="Game With Live Streaming" mainTitle="Future Of Esport"
            description="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium" />
          <!--Button group explore-->
          <div class="btn-group p-0">
            <BaseButton contentButton="EXPLORE GAMES" class="button" />
            <PlayButton />
          </div>
        </div>
        <!--Banner Soldier-->
        <div class="col-6 col-image">
          <div class="banner position-relative">
            <img src="../../assets/index-banner-illus.png" alt="soldier live" class="soldier">
          </div>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>
.row {
  height: 100%;
  align-items: center;
}

.title {
  position: relative;
  z-index: 0;
}

.controller {
  bottom: 10%;
  left: 3%;
  z-index: 0;
}

.container {
  padding-top: 75px;
  height: 100%;
}

.btn-group {
  gap: 10px;
  align-items: center;
}

.button {
  height: 56px;
}

.soldier {
  position: absolute;
  top: -500px;
  left: -30%;
}

@media (max-width: 992px) {

  .col-image,
  .controller {
    display: none;
  }

  .title {
    width: 100%;
    text-align: center;
  }


}
</style>