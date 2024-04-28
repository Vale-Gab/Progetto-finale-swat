<template>
    <div id="about-us">
        <div class="container text-center d-flex px-5">
            <div class="row">
                <div class="col-lg-6 d-flex flex-column align-items-start justify-content-center testo-sinistra">
                        <span class="pre-title">We are megaone company</span> 
                        <h2>We are making <span class="word" :class="{ 'capriola': cambiaParola }" >{{ parola }}</span> better for everyone</h2>
                        <p class="text-start">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable. If you are going to use a passage of Lorem Ipsum.</p>
                        <button class="my-btn">Learn More<span></span><span></span><span></span><span></span></button>
                </div>
                <div class="col-lg-6 mt-3 ms-0">
                    <img class="img-fluid" src="@/assets/img2.png" alt="calcoli">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutUsComponent',

    data() {
        return {
            parola: '',
            parole: ['design', 'ideas'],
            indice: 0,
        };
    },
    created() {
        this.cambiaParola();
    },

    methods: {
        cambiaParola() {
            setInterval(() => {
                this.indice = (this.indice + 1) % this.parole.length;
                this.parola = this.parole[this.indice];
            }, 2000);
        },
    },

    beforeUnmount() {
    clearInterval(this.intervallo);
},
};

</script>

<style scoped>

    .container {
        background-color: white;
        padding-top: 100px;
    }

    #about-us img {
        width: 100%;
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
        color: #00A8F5;
        font-weight: 600;
    }

    p {
        color: #696969;
        font-size: 16px;
        font-weight: 300;
        line-height: 1.8;
    }

    .my-btn {
    --c: #00A8F5;
    color: white;
    background-color: #F023B5;
    border-color: #F023B5;
    margin-top: 30px;
    padding: 10px 30px;
    }

    .my-btn:hover {
    color: white;
    background-color: transparent;
    border-color: #00A8F5;
    }

    @keyframes capriola {
        0% {
            transform: perspective(400px) rotateX(90deg);
    
        }
    
        40% {
            transform: perspective(400px) rotateX(-10deg);
        }
    
        70% {
            transform: perspective(400px) rotateX(10deg);
        }
    
        100% {
            transform: perspective(400px) rotateX(0deg);
    
        }
    }
    
    .word {
        display: inline-block;
        animation: capriola 2s ease-out infinite;
    }

</style>