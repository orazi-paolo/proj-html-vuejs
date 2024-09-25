<script>
// Import Component
import BaseSectionTitle from "../baseComponents/BaseSectionTitle.vue"

export default {
  data() {
    return {

    }
  },
  components: {
    BaseSectionTitle,
  }
}
</script>

<template>
  <!-- Streaming section  -->
  <section class="p-5">
    <div class="container w-50">
      <BaseSectionTitle contentGreen="Live Streaming" mainTitle="Watch the Streams" description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus.
      Cras ultricies ligula sed magna dictum porta." is-center />
    </div>
    <!-- Streaming video card -->
    <figure class="mx-auto my-5 position-relative">
      <img src="../../assets/video-bg.png" alt="video straming bg">
      <div class=" live-icon d-inline-flex align-items-center gap-1 rounded-4 position-absolute">
        <img src="../../assets/icon/live-icon.png" alt="live icon">
        Live
      </div>
      <div
        class="play-container text-white gap-2 d-flex flex-column justify-content-center align-items-center position-absolute">
        <div class="play-btn p-2" role="btn">
          <div class="play-icon bg-white d-flex justify-content-center align-items-center">
            <img src="../../assets/icon/play-icon.png" alt="play-icon">
          </div>
        </div>
        <h5>League of Legends</h5>
      </div>
      <div class="feedback d-inline-flex gap-4 position-absolute">
        <div class="viewers">
          <span class="nr view me-1">356,599</span>
          <span>Viewers</span>
        </div>
        <div class="likes">
          <span class="nr like me-1">23,599</span>
          <span>Likes</span>
        </div>
      </div>
    </figure>

  </section>
</template>

<style lang="scss" scoped>
section {
  background-color: black;
  background-image: url("../../assets/live-streaming-bg.png");
  background-size: contain;
  background-position: top;
  background-repeat: no-repeat;

  figure {
    width: 60%;

    img {
      max-width: 100%;
    }

    .live-icon {
      font-size: 12px;
      background-color: #FF9933;
      padding: 5px 20px;
      top: 30px;
      right: 30px;
    }

    .play-container {
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      .play-btn {
        border-radius: 50%;
        border: 1px solid #06CB7B;

        .play-icon {
          width: 50px;
          height: 50px;
          border-radius: 50%;
        }
      }

    }

    .feedback {
      font-size: 10px;
      color: white;
      left: 30px;
      bottom: 30px;

      .nr {
        color: #94CB53;
      }
    }

  }

}
</style>