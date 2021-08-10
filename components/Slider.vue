<template>
  <div class="slider relative">
    <div class="slide-text absolute w-full">
      <div class="wrap-slide-text max-w-content m-auto">
        <div class="content">
          <div class="title">
            <small>Make a better connection for</small>
            <br>
            <strong>Your Business</strong>
          </div>
          <p class="text">Mauris vel consequat felis. Curabitur id rutrum neque, ut vulputate est. Integer consectetur sed nisi et viverra. Duis in nulla erat.</p>
          <div class="btn-get-started pointer">GET STARTED</div>
        </div>
      </div>
    </div>
    <img :class="{'swap-slide': show_in_slide}" class="w-full h-auto top-0 lef-0" src="@/assets/images/slider1.jpg" alt="">
    <img :class="{'swap-slide': !show_in_slide}" class="absolute w-full h-auto top-0 lef-0" src="@/assets/images/slider2.jpg" alt="">
    <div class="pre-btn absolute flex align-center justify-end"><i class="fa fa-angle-left" aria-hidden="true"></i></div>
    <div class="next-btn absolute flex align-center"><i class="fa fa-angle-right" aria-hidden="true"></i></div>
    <div class="bottom-img w-full absolute">
      <img class="w-full" src="@/assets/images/slider-clouds.png" alt="">
    </div>  
  </div>
</template>

<script>
export default {
  data() {
    return {
      show_in_slide: true
    }
  },

  mounted() {
    let _this = this;
    setInterval(function () {
      _this.show_in_slide = !_this.show_in_slide;
    }, 9000)
  }
}
</script>

<style lang="scss">
  .slider {
    position: relative;

    .slide-text {
      height: auto;
      z-index: 50;
      top: 50%;
      transform: translateY(-50%);

      .wrap-slide-text {
        color: var(--white);
        padding: 0 35px;
        .content {
          width: 500px;
          max-width: 70%;
          .title {
            font-size: 58px;
            strong, small {
              font-family: 'Merriweather', serif !important;
            }
            small {font-size: 28px;}
          }
          .btn-get-started {
            padding: 15px 30px;
            background-color: var(--pink);
            width: fit-content;
            font-weight: bold;
            font-size: 1rem;
            margin-top: 50px;
          }
        }
      }
    }

    >img {
      top: 0;
      left: 0;
      transition: 7s;
    }

    .swap-slide {
      opacity: 0;
      visibility: hidden;
    }

    .pre-btn, .next-btn {
      width: 80px;
      height: 80px;
      background-color: rgba(255,255,255,.4);
      top: 50%;
      border-radius: 50%;
      color: var(--white);
      cursor: pointer;
      z-index: 50;

      i { font-size: 2.5rem; }
    }
    
    .pre-btn {
      left: 0;
      transform: translateY(-50%) translateX(-50%);
      i {margin-right: 20px;}
    }
    .next-btn {
      right: 0;
      transform: translateY(-50%) translateX(50%);
      i {margin-left: 20px;}
    }

    .bottom-img {
      bottom: 0;
      left: 0;
    }
  }

  @media (max-width: 1170px) {
  }

  @media (max-width: 915px) {

  }

  @media (max-width: 700px) {
    .slider {
      .slide-text {
        .wrap-slide-text {
          padding: 0 !important;
          .content {
            max-width: 80% !important;
            .title {
              font-size: 2.5rem !important;
              small {font-size: 1.2rem !important;}
            }
            .text { display: none !important;}
            .btn-get-started {margin-top: 30px !important;}
          }
        }
      }
    }
  }

  @media (max-width: 415px) {
    .slider {
      .slide-text {
        .wrap-slide-text {
          .content {
            max-width: 90% !important;
            .title {
              font-size: 1.8rem !important;
              small {font-size: 1rem !important;}
            }
            .btn-get-started {margin-top: 15px !important;}
          }
        }
      }
    }
  }
</style>
