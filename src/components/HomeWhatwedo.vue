<template>
<div>
    <b-card border-variant="0" class="mb-2 text-center bg-transparent">
        <div class="shadow img-rounded-wrapper">
            <b-img  src="https://picsum.photos/600/300/?image=25" :img-alt="item.title" width="40" height="40" class="img-rounded-center"></b-img>
        </div>
        <b-card-title class="my-4">{{ item.title }}</b-card-title>
        <b-card-text>
            {{ item.description }}
        </b-card-text>
    </b-card>
</div>
</template>

<script>
export default {
    name: "HomeWhatwedo",
    props: ['item'],
}
</script>

<style scoped>
    .img-rounded-wrapper {
        position: relative;
        width: 100px;
        height: 100px;
        border-radius: 50%;
        margin-left: auto;
        margin-right: auto;
    }
    .img-rounded-center {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 50%;
    }
</style>
