<template>
<div class="home">

    <BaseMasthead />

    <section>
        <b-container class="mt-5">
            <b-row align-v="center">
                <b-col cols="12" md="6" data-aos="slide-up" data-aos-duration="800" data-aos-delay="100">
                    <h2>Building brands on the web since 2011</h2>
                    <p class="text-muted">Oshine is fully compatible with the Woo Commerce, the most popular & free ecommerece plugin for wordpress. Showcase & Sell your products with beautiful product grids and individual product pages. </p>
                    <b-btn>Learn more</b-btn>
                </b-col>
                <b-col cols="12" md="6" data-aos="slide-up" data-aos-duration="800" data-aos-delay="100">
                    <b-img :src="'assets/images/a5.jpg'" alt="" fluid rounded></b-img>
                </b-col>
            </b-row>
        </b-container>
    </section>

    <section style="background-color: rgba(250,250,250,1);">
        <b-container class="mt-5 py-5">
            <b-row>
                <b-col class="text-center">
                    <h2>What we do</h2>
                </b-col>
            </b-row>
            <b-row class="justify-content-center">
                <b-col cols="12" md="6" class="text-center">
                    <p class="text-muted">We focus on creating clean, modern & responsive interfaces that not only look good but also work great.</p>
                </b-col>
            </b-row>
            <b-row>
                <b-col cols="12" md="6" lg="4" v-for="item in whatwedoItems" :key="item.id" data-aos="slide-up" data-aos-duration="800" data-aos-delay="100">
                    <home-whatwedo :item="item"></home-whatwedo>
                </b-col>
            </b-row>
        </b-container>
    </section>

    <section>
        <b-container fluid class="mt-5">
            <b-row>
                <b-col class="text-center">
                    <h2>Recent Work</h2>
                </b-col>
            </b-row>
            <b-row class="justify-content-center">
                <b-col cols="12" md="6" class="text-center">
                    <p class="text-muted">We focus on creating clean, modern & responsive interfaces that not only look good but also work great.</p>
                </b-col>
            </b-row>
            <b-row class="mt-4">
                <b-col cols="12" md="6" lg="4" v-for="item in workItems" :key="item.id" class="p-2 p-md-4" >
                    <home-recent-work :item="item"></home-recent-work>
                </b-col>
            </b-row>
            <b-row>
              <b-col cols="12" class="text-center"><b-btn>VIEW ALL WORK</b-btn></b-col>
            </b-row>
        </b-container>
    </section>

    <section class="testimonial mt-5" >
      <div class="custom-shape-divider-top-1649638277">
          <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
              <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill"></path>
              <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill"></path>
              <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill"></path>
          </svg>
      </div>
      <b-container class="h-100">
        <b-row align-v="center" class="justify-content-center h-100">

          <b-col cols=12 md="8">
              <BaseCarousel :items="testimonialItems"/>
          </b-col>
        </b-row>
      </b-container>
      <div class="custom-shape-divider-bottom-1649638232">
          <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
              <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill"></path>
              <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill"></path>
              <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill"></path>
          </svg>
      </div>
    </section>

    <section class="pt-4" style="background: rgba(250,250,250,1)">
      <b-container fluid>
        <b-row>
          <b-col cols=12>
            <h1>hell oworld</h1>
          </b-col>
        </b-row>
      </b-container>
    </section>


    <section class="pt-4 blog">
        <b-container class="mt-5">
            <b-row>
                <b-col class="text-center">
                    <h2>From Our Blog</h2>
                </b-col>
            </b-row>
            <b-row class="justify-content-center">
                <b-col cols="12" md="6" class="text-center">
                    <p class="text-muted">Share and subscribe for our daily blogs and articles so you wont miss any updates on the future of technology.</p>
                </b-col>
            </b-row>
            <b-row class="mt-4">
                <b-col cols="12" md="6" lg="4" v-for="item in blogItems" :key="item.id" class="p-2 p-md-4" >
                    <HomeBlogItems :item="item" :text-align="'center'" />
                </b-col>
            </b-row>
        </b-container>
    </section>


    <section class="pt-4 home-contact">
      <div class="custom-shape-divider-top-1649638277">
          <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
              <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill"></path>
              <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill"></path>
              <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill"></path>
          </svg>
      </div>
        <b-container class="mt-5">
            <b-row class="justify-content-center">
                <b-col class="text-center">
                    <b-card class="border-0 bg-primary card-home-contact">
                      <b-card-title class="text-center">Get in touch</b-card-title>
                      <b-card-text>
                        We’re currently taking on new projects. Would you like to discuss yours ? Call us at +1-123-456-7890 or mail us at help@brandexponents.com
                      </b-card-text>
                    </b-card>
                    <h2></h2>
                </b-col>
            </b-row>
        </b-container>
    </section>

</div>
</template>

<script>
// @ is an alias to /src
import HomeWhatwedo from "@/components/HomeWhatwedo.vue";
import HomeRecentWork from "@/components/HomeRecentWork.vue";
import BaseMasthead from "@/components/BaseMasthead.vue";
import BaseCarousel from "@/components/BaseCarousel.vue";
import HomeBlogItems from "@/components/HomeBlogItems.vue";
export default {
    name: 'HomeView',
    components: {
        HomeWhatwedo,
        HomeRecentWork,
        BaseMasthead,
        BaseCarousel,
        HomeBlogItems
    },
    data() {
        return {
            whatwedoItems: [{
                    id: 1,
                    title: "Ideate",
                    description: "We have crafted each demo with extensive care and the theme is power packed yet easy to use.",
                    image: "",
                },
                {
                    id: 2,
                    title: "Design",
                    description: "Oshine comes with 50+ shortcode modules that can be easily customized using Tatsu",
                    image: "",
                },
                {
                    id: 3,
                    title: "Publish",
                    description: "Quality support is what that makes Oshine one of the best selling themes of all time.",
                    image: "",
                },
            ],
            workItems: [
              {
                id: 1,
                title: "",
                description: "",
                image: "",
              },
              {
                id: 2,
                title: "",
                description: "",
                image: "",
              },
              {
                id: 3,
                title: "",
                description: "",
                image: "",
              },
              {
                id: 4,
                title: "",
                description: "",
                image: "",
              },
              {
                id: 5,
                title: "",
                description: "",
                image: "",
              },
              {
                id: 6,
                title: "",
                description: "",
                image: "",
              },
            ],
            testimonialItems: [
              {
                id: 1,
                title: "Theerawat",
                description: "Great theme and efficient support! So much choice for design layout and functionality backed up with very knowledgable support staff.",
                avatar: "https://21g6p436jemo16mo9n1a25yq-wpengine.netdna-ssl.com/v44/wp-content/uploads/sites/52/2017/08/download-14-150x150.jpg",
              },
              {
                id: 2,
                title: "Thatrawee",
                description: "This is a truly spectacular theme! The custom page builder is definitely one of the most intuitive and user-friendly page builders I’ve ever used. ",
                avatar: "https://21g6p436jemo16mo9n1a25yq-wpengine.netdna-ssl.com/v44/wp-content/uploads/sites/52/2018/08/Testimonial-person-150x150.jpg",
              }
            ],
            blogItems: [
              {
                id: 1,
                title: "Oshine – a Creative Multipurpose WordPress theme",
                date: "",
              },
              {
                id: 2,
                title: "If You Are Good At Something, Don’t Do It For Free",
                date: "",
              },
              {
                id: 3,
                title: "Woocommerce, WPML, Master Slider and much more",
                date: "",
              }
            ],
        }
    },
}
</script>

<style scoped>

.testimonial {
  height: 80vh;
  background: url('@/assets/images/bg-testimonial.jpg');
  background-position: center center;
  background-size: cover;
  position: relative;
}
.custom-shape-divider-bottom-1649638232 {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
    transform: rotate(180deg);
}

.custom-shape-divider-bottom-1649638232 svg {
    position: relative;
    display: block;
    width: calc(177% + 1.3px);
    height: 49px;
    transform: rotateY(180deg);
}

.custom-shape-divider-bottom-1649638232 .shape-fill {
    fill: rgba(250,250,250,1);

}

.custom-shape-divider-top-1649638277 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
}

.custom-shape-divider-top-1649638277 svg {
    position: relative;
    display: block;
    width: calc(177% + 1.3px);
    height: 49px;
    transform: rotateY(180deg);
}

.custom-shape-divider-top-1649638277 .shape-fill {
    fill: #FFFFFF;
}

.home-contact {
  height: 30vh;
  background: url('@/assets/images/bg-testimonial.jpg');
  background-position: center center;
  background-size: cover;
  position: relative;
}

.card-home-contact {
  margin-top: -90px;
}

</style>
