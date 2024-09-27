<script>
export default {
  data() {
    return {
      // create a object to store the data of newsLetter
      newsLetter: {
        imgButton: new URL('../../assets/icon/send-icon.png', import.meta.url).href,
        title: 'Subscribe Newsletter',
        description: 'libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus.',
      }
    }
  }
}
</script>

<template>
  <!-- create the structure of newsletter -->
  <section class="newsletter">
    <div class="container">
      <div class="row justify-content-center align-items-center">
        <div class="col-10">
          <div class="footer-form">
            <div class="row align-items-center">
              <div class="col-7">
                <h3 class="title">
                  {{ newsLetter.title }}
                </h3>
                <p>
                  {{ newsLetter.description }}
                </p>

              </div>
              <div class="col-5">
                <div class="form-group input-area d-flex align-items-center">
                  <input type="text" placeholder="Enter your email" name="input-email">
                  <button class="btn-area">
                    <a href="#header" class="transition-link">
                      <img :src="newsLetter.imgButton" alt="send">
                    </a>
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </section>
</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

.newsletter {
  position: relative;
  top: -50%;
  left: 0;
  transform: translateY(-50%);

  .footer-form {
    border-radius: $xlg;
    background-color: #30405F;
    padding: 80px 60px 72px;

    .title {
      font-weight: 700;
      margin-bottom: 10px;
      color: $white;
    }

    p {
      color: $white;
      font-size: 18px;
      font-weight: 400;
      line-height: $xlg;
    }

    .input-area {
      background-color: #425374;
      outline: 1px solid #30455f;
      border-radius: $md;

      input {
        margin: 4px;
        padding: 12px;
        border: none;
        background-color: transparent;
      }

      input,
      textarea {
        width: 100%;
        border-radius: $md;
        outline-color: #94CB53;
      }
    }
  }

  .btn-area {
    border-radius: 50%;
    background-color: #94CB53;
    min-width: 50px;
    min-height: 50px;
    cursor: pointer;
    padding: $padding-md;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .img {
    max-width: 100%;
  }
}
</style>