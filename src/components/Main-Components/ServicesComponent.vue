<template>
  <div id="services">
    <div class="container text-center p-5">
      <div class="row">
        <div class="col-md-3"><a href="#"><i class="fa-solid fa-folder-open text-center d-flex justify-content-center align-items-center"></i></a><h4>World leader in consulting and finance</h4></div>
        <div class="col-md-3"><a href="#"><i class="fa-solid fa-code text-center d-flex justify-content-center align-items-center"></i></a><h4>A focused team with a specialized skill</h4></div>
        <div class="col-md-3"><a href="#"><i class="fa-solid fa-gear text-center d-flex justify-content-center align-items-center"></i></a><h4>Trusted and professional advisors for you</h4></div>
        <div class="col-md-3"><a href="#"><i class="fa-solid fa-pen-to-square text-center d-flex justify-content-center align-items-center"></i></a><h4>Experience to give you a better results</h4></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'ServicesComponent'
}
</script>

<style scoped>

#services {
    background-color: white;
    padding: 100px 0;
}

#services a i {
    display: inline-block;
    color: white;
    font-size: 30px;
    border-radius: 50%;
    width: 80px;
    height: 80px;
    margin: 0 auto;
    text-align: center;

}

#services a i:hover {
    cursor: pointer;
    border-color: white;
    border-width: 20px;
    border: solid;
}

a {
    text-decoration: none;
}

h4 {
    font-size: 17px;
    color: #404854;
    margin-top: 20px;
}

.fa-folder-open {
    background-color: #00A8F5;
}

.fa-folder-open:hover {
    -webkit-animation: animation1 1s infinite ease-in-out;
    animation: animation1 1s infinite ease-in-out;
}

.fa-code {
    background-color: #40526B;
}

.fa-code:hover {
    -webkit-animation: animation2 1s infinite ease-in-out;
    animation: animation2 1s infinite ease-in-out;
}

.fa-gear {
    background-color: #9456F5;
}

.fa-gear:hover {
    -webkit-animation: animation3 1s infinite ease-in-out;
    animation: animation3 1s infinite ease-in-out;
}

.fa-pen-to-square {
    background-color: #EF21B5;
}

.fa-pen-to-square:hover {
    -webkit-animation: animation4 1s infinite ease-in-out;
    animation: animation4 1s infinite ease-in-out;
}


@keyframes animation1 {
    0% {
    -webkit-box-shadow: 0 0 0 5px #00a7f5f1;
    box-shadow: 0 0 0 5px #00a7f5dd;
    }
    25% {
    -webkit-box-shadow: 0 0 0 10px #00a7f5c5;
    box-shadow: 0 0 0 10px #00a7f5ac;
    }
    70% {
    -webkit-box-shadow: 0 0 0 15px #00a7f57a;
    box-shadow: 0 0 0 15px #00a7f554;
    }
    100% {
    -webkit-box-shadow: 0 0 0 60px #00a7f52e;
    box-shadow: 0 0 0 20px #00a7f50c;
    }
}

@keyframes animation2 {
    0% {
    -webkit-box-shadow: 0 0 0 5px #40526beb;
    box-shadow: 0 0 0 5px #40526bd7;
    }
    25% {
    -webkit-box-shadow: 0 0 0 10px #40526bc6;
    box-shadow: 0 0 0 10px #40526bab;
    }
    70% {
    -webkit-box-shadow: 0 0 0 15px #40526b90;
    box-shadow: 0 0 0 15px #40526b68;
    }
    100% {
    -webkit-box-shadow: 0 0 0 60px #40526b3e;
    box-shadow: 0 0 0 20px #40526b1f;
    }
}

@keyframes animation3 {
    0% {
    -webkit-box-shadow: 0 0 0 5px #9356f5ee;
    box-shadow: 0 0 0 5px #9356f5cd;
    }
    25% {
    -webkit-box-shadow: 0 0 0 10px #9356f5b4;
    box-shadow: 0 0 0 10px #9356f5a0;
    }
    70% {
    -webkit-box-shadow: 0 0 0 15px #9356f58b;
    box-shadow: 0 0 0 15px #9356f56b;
    }
    100% {
    -webkit-box-shadow: 0 0 0 60px #9356f543;
    box-shadow: 0 0 0 20px #9356f529;
    }
}

@keyframes animation4 {
    0% {
    -webkit-box-shadow: 0 0 0 5px #ef21b5e4;
    box-shadow: 0 0 0 5px #ef21b5c7;
    }
    25% {
    -webkit-box-shadow: 0 0 0 10px #ef21b5ae;
    box-shadow: 0 0 0 10px #ef21b59a;
    }
    70% {
    -webkit-box-shadow: 0 0 0 15px #ef21b581;
    box-shadow: 0 0 0 15px #ef21b566;
    }
    100% {
    -webkit-box-shadow: 0 0 0 60px #ef21b547;
    box-shadow: 0 0 0 20px #ef21b523;
    }
}

</style>
