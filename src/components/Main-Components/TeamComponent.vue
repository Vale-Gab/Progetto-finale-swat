<template>
  <div id="team" class="text-center">
    <div class="container py-4">
      <div class="row">
        <div class="col-md-12 first-part">
          <span class="pre-title">We are megaone company</span>
          <h2>We have some <span class="word" :class="{ 'capriola': cambiaParola }" >{{ parola }}</span>
             talented staff</h2>
          <p class="mb-5">
            There are many variations of passages of Lorem Ipsum available, but the majority have
            suffered alteration in some form, by injected.
          </p>
        </div>
      </div>
      <div class="row">
        <div id="div1" class="col-md-4">
          <div>
            <img src="@/assets/team-img1.png" alt="" class="img-fluid team-member" />
            <div class="nome">
              <img src="@/assets/team-hover1.png" alt="" class="img-fluid team-hover" />
              <h6>David Joe</h6>
            </div>
            <p>Director</p>
            <div>
              <a href=""><i class="fa-brands fa-facebook-f text-center p-2"></i></a>
              <a href=""><i class="fa-brands fa-linkedin-in text-center p-2"></i></a>
              <a href=""><i class="fa-brands fa-twitter text-center p-2"></i></a>
            </div>
          </div>
        </div>
        <div id="div2" class="col-md-4">
          <div>
            <img src="@/assets/team-img2.png" alt="" class="img-fluid team-member" />
            <div class="nome">
              <img src="@/assets/team-hover2.png" alt="" class="img-fluid team-hover" />
              <h6>Natalie Roy</h6>
            </div>
            <p>Director</p>
            <div>
              <a href=""><i class="fa-brands fa-facebook-f text-center p-2"></i></a>
              <a href=""><i class="fa-brands fa-linkedin-in text-center p-2"></i></a>
              <a href=""><i class="fa-brands fa-twitter text-center p-2"></i></a>
            </div>
          </div>
        </div>
        <div id="div3" class="col-md-4">
          <div>
            <img src="@/assets/team-img3.png" alt="" class="img-fluid team-member" />
            <div class="nome">
              <img src="@/assets/team-hover3.png" alt="" class="img-fluid team-hover" />
              <h6>Jhon Wok</h6>
            </div>
            <p>Director</p>
            <div>
              <a href=""><i class="fa-brands fa-facebook-f text-center p-2"></i></a>
              <a href=""><i class="fa-brands fa-linkedin-in text-center p-2"></i></a>
              <a href=""><i class="fa-brands fa-twitter text-center p-2"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamComponent',
  data() {
        return {
            parola: 'ideal',
            parole: ['ideal', 'great'],
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

#team {
  background-color: #ffffff !important;
  padding: 100px 0;
}

#div1:hover,
#div2:hover,
#div3:hover {
  h6 {
    color: white;
  }
  .team-hover {
    opacity: 100;
    z-index: 1;
    cursor: pointer;
  }
  .nome:hover {
    cursor: pointer;
  }
}

#team .team-member {
  width: 250px;
  height: 250px;
  margin-bottom: 30px;
  transition: transform 0.2s;
}

#team a i {
  margin: 0 5px;
  display: inline-block;
  color: #404854;
  background-color: white;
  height: 30px;
  width: 30px;
  font-size: 16px;
}

#team a i:hover {
  background-color: #00a8f5;
  color: white;
  border-radius: 50%;
  display: inline-block;
}

.first-part {
  width: 550px;
  margin: 0 auto;
}

.team-member:hover {
  -ms-transform: scale(1.1);
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
  cursor: pointer;
}

h2 {
  font-size: 40px;
  font-weight: 600;
  color: #404854;
  margin: 25px 0;
}

h6 {
  font-size: 23px;
  color: #404854;
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.team-hover {
  opacity: 0;
  transition: all 0.3s ease-in-out;
  overflow: clip;
}

.nome {
  position: relative;
}

p {
  font-size: 16px;
  color: #696969;
  font-weight: 300;
  line-height: 1.8;
}

.pre-title span {
  color: #696969;
  font-size: 18px;
  margin-bottom: 25px;
}

#team .pre-title {
  color: #696969;
  font-size: 18px;
}

.word {
  color: #00a8f5;
  font-weight: 600;
  transition: ease-in-out 0.2s;
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
