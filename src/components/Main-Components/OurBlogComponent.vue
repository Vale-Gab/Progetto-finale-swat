<template>
    <div id="our-blog" class="bg-light">
        <div class="container">
            <div class="row">
                <div class="col-md-12 text-center">
                    <span class="pre-title">We are megaone company</span>
                    <h2>Our <span class="rotation-word"> latest blogs</span> will keep everyone updated</h2>
                </div>
            </div>
            <div class="row mt-5">
                <div class="col-lg-4">
                    <div class="card">
                        <img src="@/assets/blog-news-1.jpg" class="card-img-top img-fluid" alt="news">
                    <div class="card-body p-4">
                        <span class="date">October 29, 2023</span>
                        <h4 class="card-title my-3">Web design is fun</h4>
                        <p class="card-text">Lorem ipsum dolor sit amet consectetur adipiscing elit ipsum dolor sit am...</p>
                        <div class="foot-card d-flex align-items-center">
                            <img src="@/assets/avatar-1.png" alt="" class="avatar1 img-fluid">
                            <h6>Valeria Gabriele</h6>
                        </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-4">
                    <div class="card">
                        <img src="@/assets/blog-news-2.jpg" class="card-img-top img-fluid" alt="news">
                    <div class="card-body p-4">
                        <span class="date">October 29, 2023</span>
                        <h4 class="card-title my-3">Future of websites</h4>
                        <p class="card-text">Lorem ipsum dolor sit amet consectetur adipiscing elit ipsum dolor sit am...</p>
                        <div class="foot-card d-flex align-items-center">
                            <img src="@/assets/avatar-2.png" alt="" class="avatar2 img-fluid">
                            <h6>Tom Welling</h6>
                        </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-4">
                    <div class="card">
                        <img src="@/assets/blog-news-3.jpg" class="card-img-top img-fluid" alt="news">
                    <div class="card-body p-4">
                        <span class="date">October 29, 2023</span>
                        <h4 class="card-title my-3">Digital marketing</h4>
                        <p class="card-text">Lorem ipsum dolor sit amet consectetur adipiscing elit ipsum dolor sit am...</p>
                        <div class="foot-card d-flex align-items-center">
                            <img src="@/assets/avatar-3.png" alt="" class="avatar3 img-fluid">
                            <h6>Viola Doe</h6>
                        </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'OurBlogComponent'
}
</script>

<style scoped>

#our-blog {
    padding: 100px 0;
}

.pre-title {
    color: #696969;
    font-size: 18px;
    margin-bottom: 25px;
}

h2 {
    font-size: 40px;
    font-weight: 600;
    color: #404854;
    margin: 25px auto;
    width: 550px;
}

.rotation-word {
    color: #00a8f5;
    font-weight: 600;
}

.p-title {
    color: #696969;
    font-size: 16px;
    font-weight: 300;
    line-height: 1.8;
    width: 500px;
    margin: 25px auto;
}

.avatar1, .avatar2, .avatar3 {
    border-radius: 50%;
    width: 50px;
    margin-right: 15px;
}

.avatar1 {
    background-color: #00a8f5;
}

.avatar2 {
    background-color: #9456F5;
}

.avatar3 {
    background-color: #f033b5;
}

.date {
    color: #F033B5;
    font-size: 16px;
}

.card-text {
    color: #696969;
    font-size: 16px;
    font-weight: 300;
    line-height: 1.8;
}

h6 {
    color: #404854;
    font-size: 15px;
    margin-bottom: 0;
    transition: 0.2s;
}

h6:hover {
    color: #00a8f5;
    cursor: pointer;
}

.card {
    border: none;
    transition: all ease-in-out 0.3s;
    border-radius: 10px;
    padding-bottom: 20px;
}

.card:hover {
    box-shadow: 0px 4px 8px rgba(137, 136, 136, 0.2);
    top: -7px;
}

.card-title:hover {
    color: #00a8f5;
    cursor: pointer;
}

.card-img-top {
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}


</style>