<template>
  <div class="dash-galery">
    <h3>Event Galleries</h3>
    <swiper :navigation="true" :modules="modules" class="mySwiper">
      <swiper-slide  v-for="(item, ind) in images">
        <img class="imgGalery" :src="item.url" alt="Galery one">
        <span class="title-slide">SLIDE {{ind + 1}}</span>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/navigation';


  // import required modules
  import { Navigation } from 'swiper';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation],

        images: [
          {
            url: '/src/assets/img/img-galery-1.jpg'
          },
          {
            url: '/src/assets/img/img-galery-2.jpg'
          },
          {
            url: '/src/assets/img/img-galery-3.jpg'
          }
        ]
      };
    },
  };
</script>

<style lang="scss">
@import '../../../assets/modules/mixins';

.swiper {
  max-width: 879px;
  height: 100%;
  max-height: 555px;
  border-radius: 25px;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title-slide {
  position: absolute;
  color: #fff;
  bottom: 12%;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.imgGalery {
  width: 100%;
}

.dash-galery {
  h3 {
    color: #fff;
    font-size: 36px;
    line-height: 55px;

    @include media('mobile') {
      text-align: center;
      font-size: 1em;
    }
  }
}

.swiper-button-prev {
  top: initial;
  bottom: 10% !important;
  left: 25%;

  @include media('mobile') {
    left: 5%;
  }
}

.swiper-button-next {
  top: initial;
  bottom: 10% !important;
  right: 25%;
  @include media('mobile') {
    right: 5%;
  }
}

.swiper-button-prev::after {
  content: url('/src/assets/svg/arrow-right-icon.svg');
  transform: rotate(180deg);
}

.swiper-button-next::after {
  content: url('/src/assets/svg/arrow-right-icon.svg');
  
}

</style>
