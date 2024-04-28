<template>
    <footer id="footer" class="bg-light">
        <div>
            <button id="scrollUp" class="btn" @click="scrollToTop"><i class="fas fa-angle-up"></i></button>
        </div>
        <div class="container">
            <div class="row footer">
                <div class="col-lg-6">
                    <ul class="social d-flex text-center">
                        <li><i class="fa-brands fa-facebook-f text-center"></i></li>
                        <li><i class="fa-brands fa-twitter text-center"></i></li>
                        <li><i class="fa-brands fa-google-plus-g text-center"></i></li>
                        <li><i class="fa-brands fa-linkedin-in text-center"></i></li>
                        <li><i class="fa-brands fa-instagram text-center"></i></li>
                        <li><i class="fa-brands fa-pinterest-p text-center"></i></li>
                    </ul>
                </div>
                <div class="col-lg-6 text-end">
                    <p>© 2024 MegaOne. Made With Love By <span>Valeria Gabriele</span></p>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterComponent',
    data() {
    return {
        showBackToTopButton: false
    };
    },
    methods: {
  scrollToTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
}
}
</script>

<style scoped>

#scrollUp {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #643094;
    color: white;
    border: none;
    border-radius: 50%;
    width: 45px;
    height: 45px;
    text-align: center;
    font-size: 22px;
    cursor: pointer;
}

#scrollUp:hover{
    background-color: #00bcd4;
}

#footer {
    padding: 80px 0;
    display: flex;
    align-items: center;
}

.social {
    list-style-type: none;
    color: #696969;
}

.fa-brands{
    margin-right: 15px;
    font-size: 18px;
    border-radius: 50%;
    display: inline-block;
    width: 40px;
    height: 40px;
    padding: 10px;
}

.fa-brands:hover {
    margin-right: 15px;
    font-size: 18px;
    border-radius: 50%;
    display: inline-block;
    width: 40px;
    height: 40px;
    color: white;
    cursor: pointer;
    background-color: #00BCD4;
    display: inline-block;
    padding: 10px;
}

p, span {
    color: #696969;
    font-weight: 300;
    font-size: 14px;
}

span:hover {
    color: #00A8F5;
    cursor: pointer;
}




</style>