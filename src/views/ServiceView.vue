<template>
  <div class="service">
    <BaseMasthead :title="titleHead"/>
    <b-container>
      <b-row class="mt-5">
        <b-col cols=12>
          <h1 class="text-center">This is an service page</h1>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import BaseMasthead from '@/components/BaseMasthead.vue'
export default {
  name: "ServiceView",
  components: {
    BaseMasthead,
  },
  data() {
      return {
          titleHead: "This is Service Page",
      }
  },
}
</script>
