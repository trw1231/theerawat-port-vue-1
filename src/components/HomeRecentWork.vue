<template>
    <div>
        <!-- <b-card
            overlay
            img-src="https://picsum.photos/900/250/?image=3"
            img-alt="Card Image"
            text-variant="white"
            title="Image Overlay"
            sub-title="Subtitle"
            class="border-0"
        >
            <b-card-text>
            Some quick example text to build on the card and make up the bulk of the card's content.
            </b-card-text>
        </b-card> -->

        <div class="custom-overlay-wrapper">
            <img src="https://picsum.photos/900/250/?image=3"  alt="">
              <div class="card__overlay">
                    <div class="overlay__text">
                    <h3>{{item.title}}</h3>
                    </div>
              </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "HomeRecentWork",
    props: ['item']
}
</script>

<style scoped>
    .custom-overlay-wrapper {
        width: 100%;
        height: 250px;
        position: relative;
    }

    .custom-overlay-wrapper img {
        width: 100%;
        height: 100%;
        display: block
    }
    .card__overlay {
        position: absolute;
        top: 50%;
        /* bottom: 0; */
        left: 50%;
        /* right: 0; */
        height: 95%;
        width: 98%;
        opacity: 0;
        visibility: none;
        transition: .5s ease;
        background-color: #ffffff;
        transform: translate(-50%, -50%);
        text-align: center;
    }
    .overlay__text {
        display: flex;
        height: 100%;
        justify-content: center;
        align-items: center;
    }

    .custom-overlay-wrapper:hover .card__overlay {
        opacity: 1;
    }
</style>