<template>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="item in items" :key="item.id" style="width: 100%; height: 450px; background-color: transparent;">
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
    name: 'BaseCarousel',
    props: ["items"],
    data() {
      return {
        swiperOptions: {
          slidesPerView: 1,
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