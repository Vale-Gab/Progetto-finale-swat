<template>
    <div id="clients" class="text-center gradient-bg1">
        <div class="container">
            <i class="fa-solid fa-quote-left fa-2xl"></i>
            <div class="row">
                <div class="col-md-12">
                    <div class="title-area">
                        <h2>
                            Some <span class="rotation-word">ideal</span> words from our clients
                        </h2>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-md-12">
                    <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
                        <div class="carousel-inner">
                    <div class="carousel-item active">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse tincidunt
                            egestas nunc, at pellentesque arcu sollicitudin et. Aliquam hendrerit diam quis ipsum
                            ultricies, quis ultricies arcu suscipit. Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit. Fusce ut diam quis nulla faucibus venenatis.</p>
                        <h5 class="name gradient-text1">David Villas</h5>
                        <span class="designation">Designer, Company Name</span>
                        <ul class="stars d-flex text-center">
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                        </ul>
                    </div>
                    <div class="carousel-item">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse tincidunt
                            egestas nunc, at pellentesque arcu sollicitudin et. Aliquam hendrerit diam quis ipsum
                            ultricies, quis ultricies arcu suscipit. Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit. Fusce ut diam quis nulla faucibus venenatis.</p>
                        <h5 class="name gradient-text1">David Villas</h5>
                        <span class="designation">Designer, Company Name</span>
                        <ul class="stars d-flex text-center">
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                        </ul>
                    </div>
                    <div class="carousel-item">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse tincidunt
                            egestas nunc, at pellentesque arcu sollicitudin et. Aliquam hendrerit diam quis ipsum
                            ultricies, quis ultricies arcu suscipit. Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit. Fusce ut diam quis nulla faucibus venenatis.</p>
                        <h5 class="name gradient-text1">David Villas</h5>
                        <span class="designation">Designer, Company Name</span>
                        <ul class="stars d-flex text-center">
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                            <li><i class="fa-solid fa-star me-1"></i></li>
                        </ul>
                    </div>
                    </div>
                    <a class="carousel-control-prev1" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-1.png" alt="" class="avatar1 img-fluid">
                        </span>
                        <span class="visually-hidden">Previous</span>
                    </a>
                    <a class="carousel-control-prev2" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-2.png" alt="" class="avatar2 img-fluid">
                        </span>
                        <span class="visually-hidden">Previous</span>
                    </a>
                    <a class="carousel-control-prev3" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-3.png" alt="" class="avatar3 img-fluid">
                        </span>
                        <span class="visually-hidden">Previous</span>
                    </a>
                    <a class="carousel-control-prev4" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-4.png" alt="" class="avatar4 img-fluid">
                        </span>
                        <span class="visually-hidden">Previous</span>
                    </a>
                    <a class="carousel-control-next1" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-5.png" alt="" class="avatar5 img-fluid">
                        </span>
                        <span class="visually-hidden">Next</span>
                    </a>
                    <a class="carousel-control-next2" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-6.png" alt="" class="avatar6 img-fluid">
                        </span>
                        <span class="visually-hidden">Next</span>
                    </a>
                    <a class="carousel-control-next3" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-7.png" alt="" class="avatar7 img-fluid">
                        </span>
                        <span class="visually-hidden">Next</span>
                    </a>
                    <a class="carousel-control-next4" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
                        <span aria-hidden="true">
                            <img src="@/assets/avatar-1.png" alt="" class="avatar8 img-fluid">
                        </span>
                        <span class="visually-hidden">Next</span>
                    </a>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: 'ClientsComponent'
}
</script>

<style scoped>

.gradient-bg1 {
    background: #3264f5;
    background: -moz-linear-gradient(left, #3264f5 2%, #7004bc 82%);
    background: -webkit-linear-gradient(left, #3264f5 2%, #7004bc 82%);
    background: linear-gradient(to right, #3264f5 2%, #7004bc 82%);
    position: relative;
    padding: 120px 0;
}

.fa-quote-left {
    color: rgba(255, 255, 255, 0.105);
    font-size: 300px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 0;

}

h2 {
    font-size: 40px;
    color: white;
    font-weight: 600;
    text-align: center;
    margin: 0 auto;
    width: 700px;
}

.avatar1, .avatar2, .avatar3, .avatar4, .avatar5, .avatar6, .avatar7, .avatar8 {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    padding: 6px;
    background-color: white;
    position: absolute;
    z-index: 1;
}

.avatar1 {
    top: -60px;
    left: -70px;
}

.avatar2 {
    top: 0;
    left: 90px;
}

.avatar3 {
    top: 130px;
    left: -35px;
}

.avatar4 {
    bottom: 20px;
    left: 120px;
}

.avatar5 {
    top: -80px;
    right: 120px;
}

.avatar6 {
    top: -30px;
    right: -60px;
}

.avatar7 {
    top: 60px;
    right: 70px;
}

.avatar8 {
    bottom: 20px;
    right: 150px;
}

a img:hover {
    -webkit-animation: animation1 1s infinite ease-in-out;
    animation: animation1 1s infinite ease-in-out;
    cursor: pointer;
}

@keyframes animation1 {
    0% {
    -webkit-box-shadow: 0 0 0 5px rgba(255, 255, 255, 0.919);
    box-shadow: 0 0 0 5px rgba(255, 255, 255, 0.762);
    }
    25% {
    -webkit-box-shadow: 0 0 0 10px rgba(255, 255, 255, 0.605);
    box-shadow: 0 0 0 10px rgba(255, 255, 255, 0.517);
    }
    70% {
    -webkit-box-shadow: 0 0 0 15px rgba(255, 255, 255, 0.453);
    box-shadow: 0 0 0 15px rgba(255, 255, 255, 0.335);
    }
    100% {
    -webkit-box-shadow: 0 0 0 60px rgba(255, 255, 255, 0.195);
    box-shadow: 0 0 0 20px rgba(255, 255, 255, 0.074);
    }
}

.carousel-item p {
    font-size: 18px;
    color: white;
    font-weight: 300;
    text-align: center;
    margin: 40px auto;
    width: 700px;
    font-style: italic;
    line-height: 1.8;
}

.gradient-text1 {
    background: #f033b5;
    background: -moz-linear-gradient(left, #f033b5 2%, #f2a2af 82%);
    background: -webkit-linear-gradient(left, #f033b5 2%, #f2a2af 82%);
    background: linear-gradient(to right, #f033b5 2%, #f2a2af 82%);
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f033b5', endColorstr='#f2a2af',GradientType=1 );
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: 600;
    font-size: 20px;
}

.designation {
    font-size: 15px;
    color: white;
    font-weight: 300;
    text-align: center;
    margin-top: 10px;
}

.stars {
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-left: 0;
    margin-top: 20px;
    color: #FECE21;
}

.rotation-word {
    font-weight: 600;
}

</style>