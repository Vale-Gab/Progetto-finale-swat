<template>
    <div id="sponsor" class="gradient-bg2">
        <div class="container">
            <div class="envato-slider d-flex" id="slider">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
                <img src="@/assets/sponsor.png" alt="" srcset="">
            </div>
            </div>
        </div>
</template>

<script>
export default {
    name: 'SponsorComponent'
}
</script>

<style scoped>

.envato-slider img {
    margin-right: 100px;
    animation: slide 4s linear infinite;
}

.container {
    width: 1000px;
    overflow: hidden;
    position: relative;
}

@keyframes slide {
    0% {
        transform: translate3d(0);
    }
    25% {
        transform: translate3d(-240px, 0px, 0px); 
    }
    50% {
        transform: translate3d(-240px, 0px, 0px); 
    }
    75% {
        transform: translate3d(-240px, 0px, 0px); 
    }

    100% {
        transform: translate3d(-240px, 0px, 0px); 
    }
}

.gradient-bg2 {
    background: #237afe;
    background: -moz-linear-gradient(left, #237afe 2%, #03a9f5 82%);
    background: -webkit-linear-gradient(left, #237afe 2%, #03a9f5 82%);
    background: linear-gradient(to right, #237afe 2%, #03a9f5 82%);
    padding: 100px 0 360px 0;
}

</style>