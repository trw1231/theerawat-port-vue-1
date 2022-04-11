<template>
  <div>
    <b-card
        :title="item.title"
        :img-src="item.image"
        :img-alt="item.title+'-image'"
        img-top
        class="mb-2 text-center border-0"
    >

    </b-card>
  </div>
</template>

<script>
export default {
    name: "HomeBlogItems",
    props: ['item', 'text-align'],
}
</script>

<style>

</style>