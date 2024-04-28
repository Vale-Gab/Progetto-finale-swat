<template>
  <div id="jumbtron">
    <div ref="follower" id="mouse-follower"></div>
    <div class="container text-center pt-5 d-flex">
      <div class="gradient-bg1 bg-overlay"></div>
      <div class="row pt-5">
        <div class="col-lg-6 mt-5 ms-0 lato-sinistro">
          <img class="img-fluid animated" src="@/assets/img1.png" alt="scrivania" />
        </div>
        <div
          class="col-lg-6 d-flex flex-column align-items-start justify-content-center lato-destro"
        >
          <h1>
            <span class="gradient-text">Creative<br /></span> Digital Agency
          </h1>
          <p>
            Lorem ipsum dolor sit amet consectetur a dipisicing elit. Laudantium nesciunt blanditiis
            dolor praesentium? Ut labore consectetur iure dignissimos accusantium in, quae minus est
            at corrupti.
          </p>
          <button class="my-btn">
            Learn More<span></span><span></span><span></span><span></span>
          </button>
        </div>
      </div>
      <div class="scroll-down"><a href="#about-us">Scroll Down &#x2193;</a></div>
      <img src="@/assets/cerchio.png" alt="cerchio" class="cerchio img-fluid" />
    </div>
    <img
      src="@/assets/rettangolo.png"
      alt="rettangolo"
      class="rettangolo img-fluid"
      @click="openPanel"/>

    <div v-if="isPanelOpen" class="side-panel">
      <div class="closex" @click="closePanel">X</div>
      <ul class="mpanel">
        <li>
          <a href="#">
            <span class="panel-circle"></span>
            Home
          </a>
        </li>
        <li>
          <a href="#about-us">
            <span class="panel-circle"></span>
            About
          </a>
        </li>
        <li>
          <a href="#portfolio">
            <span class="panel-circle"></span>
            Work
          </a>
        </li>
        <li>
          <a href="#clients">
            <span class="panel-circle"></span>
            Clients
          </a>
        </li>
        <li>
          <a href="#our-blog">
            <span class="panel-circle"></span>
            Blog
          </a>
        </li>
        <li>
          <a href="#contact-us" class="contact">
            <span class="panel-circle"></span>
            Contact
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'JumbtronComponent',

  data() {
    return {
      isPanelOpen: false
    }
  },

  methods: {
    openPanel() {
      this.isPanelOpen = true
    },
    closePanel() {
      this.isPanelOpen = false
    }
  },

  mounted() {
    const follower = this.$refs.follower

    const cursorAnimateEvent = (elements) => {
      window.addEventListener('mousemove', (e) => {
        elements.forEach((element) => {
          element.name.style.display = e.pageY < 910 ? null : 'none'

          element.name.animate(
            [
              {
                opacity: 1,
                left: `${e.pageX}px`,
                top: `${e.pageY}px`
              }
            ],
            {
              duration: element.duration,
              fill: 'forwards'
            }
          )
        })
      })

      window.addEventListener('mouseout', () => {
        elements.forEach((element) => {
          element.name.animate(
            [
              {
                opacity: 1
              }
            ],
            {
              duration: element.fadeOut,
              fill: 'forwards'
            }
          )
        })
      })
    }

    cursorAnimateEvent([
      {
        name: follower,
        duration: 1000,
        fadeOut: 100
      }
    ])
  }
}
</script>

<style scoped>
#jumbtron {
  height: 100vh;
  width: 100vw;
  overflow-x: hidden;
  position: relative;
}

#mouse-follower {
  opacity: 1;
  top: -10px;
  left: -10px;
  transform: translate(-50%, -50%);
  position: fixed;
  transition: 90ms ease-in-out;
  pointer-events: none;
  height: 30px;
  width: 30px;
  border: 2px solid white;
  border-radius: 50%;
  position: absolute;
}

h1,
h1 .gradient-text {
  font-size: 60px;
  font-weight: 800;
  font-family: 'Montserrat', sans-serif;
  color: white;
  text-align: start;
}

p {
  font-size: 18px;
  color: white;
  font-weight: 300;
  text-align: start;
  margin-top: 30px;
}

.gradient-bg1 {
  background: #3264f5;
  background: -moz-linear-gradient(left, #3264f5 2%, #7004bc 82%);
  background: -webkit-linear-gradient(left, #3264f5 2%, #7004bc 82%);
  background: linear-gradient(to right, #3264f5 2%, #7004bc 82%);
}

.bg-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

.gradient-text {
  background: #f033b5;
  background: -moz-linear-gradient(left, #f033b5 2%, #f2a2af 82%);
  background: -webkit-linear-gradient(left, #f033b5 2%, #f2a2af 82%);
  background: linear-gradient(to right, #f033b5 2%, #f2a2af 82%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f033b5', endColorstr='#f2a2af',GradientType=1 );
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.my-btn {
  --c: white;
  color: white;
  background-color: #00a8f5;
  border-color: #00a8f5;
  margin-top: 30px;
  padding: 10px 30px;
}

.my-btn:hover {
  color: black;
  background-color: transparent;
  border-color: white;
}

.scroll-down {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  color: white;
  font-size: 20px;
  font-weight: 500;
  font-family: 'Montserrat', sans-serif;
}

.scroll-down a {
  color: white;
  text-decoration: none;
}

.animated {
  animation: move 4s ease-in-out infinite alternate-reverse;
}

@keyframes move {
  0% {
    transform: translateX(20px);
  }
  100% {
    transform: translateX(-20px);
  }
}

.cerchio {
  position: absolute;
  right: -400px;
  top: 30%;
}

.rettangolo {
  position: absolute;
  left: -400px;
  top: 7px;
  width: 650px;
}

.closex {
  font-size: 24px;
  color: white;
  text-decoration: none;
  cursor: pointer;
  position: absolute;
  top: 270px;
  left: 200px;
  z-index: 300;
}

.side-panel ul li a {
  color: white;
  padding: 10px 0;
  text-decoration: none;
  line-height: 3;
}

ul {
  list-style: none;
  padding-left: 0;
  margin-left: 0;
}

.mpanel {
  transform: translateY(-450px);
  margin-left: 30px;
  font-family: "Montserrat", sans-serif;
  font-size: 18px;
}

.panel-circle {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  border: 1px solid white;
  display: inline-block;
  margin-right: 10px;
}

.panel-circle:hover {
    background-color: white;
  }

</style>
