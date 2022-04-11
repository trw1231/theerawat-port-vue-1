<template>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="item in items" :key="item.id" style="width: 100%; background-color: transparent;">
        <p class="text-center text-white mt-auto" style="font-size: 24px;">
            {{item.description}}
        </p>
        <div class="img-testimonial-wrapper text-center" v-if="item.avatar">
            <b-img :src="item.avatar" :alt="item.title" class="rounded-circle text-center"></b-img>
        </div>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
  export default {
    name: 'HomeTestimonialCarousel',
    props: ["items"],
    data() {
      return {
        swiperOptions: {
          loop: true,
          slidesPerView: 1,
          // pagination: {
          //   el: '.swiper-pagination'
          // },
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

<style scoped> 
.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  flex-direction: column;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 80px;
  height: 80px;
}
  
</style>