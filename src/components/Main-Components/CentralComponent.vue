<template>
    <div id="central">
        <div class="container text-center d-flex py-4">
            <div class="row">
                <div class="col-lg-6 d-flex flex-column align-items-start justify-content-center testo-sinistra">
                    <span class="pre-title">We are megaone company</span> 
                        <h2><span class="rotation-word">Creative Idea</span> and Development Solutions</h2>
                        <p class="text-start">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable. If you are going to use a passage of Lorem Ipsum.</p>
                        <button class="my-btn">Learn More<span></span><span></span><span></span><span></span></button>
                </div>
                <div class="col-lg-6 ms-0">
                    <img class="img-fluid" src="@/assets/img4.png" alt="brindisi">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CentralComponent'
}
</script>

<style scoped>

    #central {
        background-color: #F8F9FA;
        padding: 100px 0;
    }

    .pre-title {
        color: #696969;
        font-size: 18px;
        margin-bottom: 25px;
    }

    h2 {
        text-align: start;
        font-size: 40px;
        font-weight: 600;
        color: #404854;
        margin-bottom: 25px;
    }

    h2 span {
        color: #F023B5;
        font-weight: 600;
    }

    p {
        color: #696969;
        font-size: 16px;
        font-weight: 300;
        line-height: 1.8;
    }

    .my-btn {
    --c: #F023B5;
    color: white;
    background-color: #00A8F5;
    border-color: #00A8F5;
    margin-top: 30px;
    padding: 10px 30px;
    }

    .my-btn:hover {
    color: white;
    background-color: transparent;
    border-color: #F023B5;
    }

</style>