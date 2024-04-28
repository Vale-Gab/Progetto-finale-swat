<template>
    <div id="location">
        <div class="container">
            <div class="row">
                <div class="col-lg-12 text-center">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d202405.6536350754!2d126.80933336507611!3d37.56476155673628!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x357ca2012d5c39cf%3A0x7e11eca1405bf29b!2sSeul%2C%20Corea%20del%20Sud!5e0!3m2!1sit!2sit!4v1712570249199!5m2!1sit!2sit" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LocationComponent'
}
</script>

<style scoped>

    #location {
        padding: 100px 0;
    }

    iframe {
        width: 100%;
        height: 500px;
        margin-top: -350px;
    }

</style>