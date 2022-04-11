<template>
  <div>
    <b-card
        :title="item.title"
        img-src="https://picsum.photos/600/300/?image=25"
        img-alt="Image"
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