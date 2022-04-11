<template>
  <swiper ref="mySwiper" class="logoCarousel" :options="swiperOptions">
    <swiper-slide v-for="item in items" :key="item.id" align-v="center">
        <div class="img-testimonial-wrapper text-center" v-if="item.image">
                <div v-html="item.image"></div>
            <!-- <b-img :src="item.image" class="text-center"></b-img> -->
        </div>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<style scoped>


.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: transparent;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
  height: 300px;
}
</style>

<script>
  export default {
    name: 'BaseCarousel',
    props: ["items"],
    data() {
      return {
        swiperOptions: {
          breakpoints: {
          '640': {
            slidesPerView: 1,
            spaceBetween: 20,
          },
          '768': {
            slidesPerView: 3,
            spaceBetween: 40,
          },
          '1024': {
            slidesPerView: 4,
            spaceBetween: 50,
          },
          },
          loop: true,
          pagination: {
            el: '.swiper-pagination'
          },
          // Some Swiper option/callback...
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },
    mounted() {
      console.log('Current Swiper instance object', this.swiper)
    }
  }
</script>