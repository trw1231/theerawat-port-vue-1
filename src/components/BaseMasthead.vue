<template>
      <section class="hero">
        <b-container class="h-100">
          <b-row align-v="center" class="h-100 justify-content-center">
            <b-col cols="12" md="8">
              <h1 class="display-4 font-weight-bold text-center">Creative Agency based out of London, UK</h1>
            </b-col>
          </b-row>
          <b-row>

          </b-row>
        </b-container>
        <div class="custom-shape-divider-bottom-1649634725">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M600,112.77C268.63,112.77,0,65.52,0,7.23V120H1200V7.23C1200,65.52,931.37,112.77,600,112.77Z" class="shape-fill"></path>
            </svg>
        </div>
    </section>
</template>

<script>
export default {
    name: "BaseMasthead",
}
</script>

<style scoped>
.hero {
    background: #115d98;
    position: relative;
    color: #fff;
    height: 80vh;
    background: url('@/assets/images/bg-masthead.jpg'); 
    background-size: cover; 
    background-position: center center; 
    background-repeat: no-repeat
}

.custom-shape-divider-bottom-1649634725 {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
}

.custom-shape-divider-bottom-1649634725 svg {
    position: relative;
    display: block;
    width: calc(100% + 1.3px);
    height: 81px;
}

.custom-shape-divider-bottom-1649634725 .shape-fill {
    fill: #FFFFFF;
}

</style>