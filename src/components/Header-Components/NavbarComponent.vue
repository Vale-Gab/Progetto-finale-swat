<template>
  <header class="fixed-top">
    <nav class="navbar navbar-expand-lg py-3 px-5" id="navbar" :class="{ 'fadeInDown': isNavBarVisible, 'fixed-top2': isNavBarFixed }">
      <div class="mouse-circle" :style="{ left: x + 'px', top: y + 'px' }"></div>
      <div ref="follower" class="follower"></div>
      <div class="container-fluid">
        <div class="wrapper-menu me-5" @click="toggleMenu" :class="{ open: isOpen }">  
          <div class="line-menu half start"></div>
          <div class="line-menu"></div>
          <div class="line-menu half end"></div>
        </div>
        <img src="@/assets/logo.png" alt="logo" class="logo"/>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav ms-auto d-flex align-items-center justify-content-center">
            <a class="nav-link me-4 sottolineato" aria-current="page" href="#jumbtron">Home</a>
            <a class="nav-link me-4 sottolineato" href="#about-us">About Us</a>
            <a class="nav-link me-4 sottolineato" href="#portfolio">Our Work</a>
            <a class="nav-link me-4 sottolineato" href="#clients">Clients</a>
            <a class="nav-link me-4 sottolineato" href="#our-blog">Our Blog</a>
            <a class="nav-link me-4 sottolineato" href="#contact-us">Contact Us</a>
            <a class="nav-link" href="#" @click="openModal">
              <button class="my-btn me-1">
                Get A Quote<span></span><span></span><span></span><span></span>
              </button>
            </a>
            <a class="nav-link me-1 d-flex align-items-center" href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a class="nav-link me-1 d-flex align-items-center" href="#"><i class="fa-brands fa-instagram"></i></a>
            <a class="nav-link d-flex align-items-center" href="#"><i class="fa-brands fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </nav>
  </header>
  <Modal :show="show" @close="closeModal" :modalContentStyle="modalContentStyle">
    <span class="pre-title">We are megaone company</span>
    <h2>Lets start your <span class="rotation-word">project</span></h2>
    <div class="form">
      <div class="row">
        <div class="col-md-6">
          <input type="text" class="form-control mb-3" placeholder="Name" aria-label="Name">
          <input type="text" class="form-control mb-3" placeholder="Contact #" aria-label="Contact">
          <input type="text" class="form-control mb-3" placeholder="Project Type" aria-label="Project">
        </div>
        <div class="col-md-6">
          <input type="email" class="form-control mb-3" placeholder="Email" aria-label="Email">
          <input type="text" class="form-control mb-3" placeholder="City/Country" aria-label="City">
          <input type="text" class="form-control mb-3" placeholder="Budget" aria-label="Budget">
        </div>
        <div class="col-12 text-start">
          <textarea class="form-control" id="exampleFormControlTextarea1" rows="8" placeholder="Please explain your project in detail."></textarea>
        </div>
        <div class="col-12">
          <div class="form-check d-flex justify-content-center align-items-center">
            <input class="form-check-input" type="checkbox" id="gridCheck">
            <label class="form-check-label" for="gridCheck">
              Contact by phone
            </label>
          </div>
        </div>
        <div class="col-12">
          <button type="submit" class="btn my-btn2">Send Message<span></span><span></span><span></span><span></span></button>
        </div>
      </div>
    </div>
  </Modal>
</template>

<script>
import ModalComponent from './ModalComponent.vue'
export default {
  name: 'NavbarComponent',
  components: {
    Modal: ModalComponent
  },
  data() {
    const modalContentStyle = `
    background-color: #fefefe;
    margin: 60px auto;
    padding: 20px 150px;
    border: none;
    width: 60%;
    height: 85%;
    text-align: center;
    `
    return {
      isOpen: false,
      show: false,
      modalContentStyle: modalContentStyle,
      isNavBarVisible: false,
      isNavBarFixed: false,
      x: 0,
      y: 0,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
    window.addEventListener('mousemove', this.updatePosition);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
    window.removeEventListener('mousemove', this.updatePosition);
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen
    },
    openModal() {
      this.show = true
    },
    closeModal() {
      this.show = false
    },

    handleScroll() {
      if (window.scrollY > 400) {
        this.isNavBarVisible = true;
        this.isNavBarFixed = true;
      } else {
        this.isNavBarVisible = false;
        this.isNavBarFixed = false;
      }
    },

    updatePosition(e) {
        const navbar = document.getElementById('navbar');
        const rect = navbar.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;

    if (x >= rect.left && x <= rect.right && y >= rect.top && y <= rect.bottom) {

      const circleX = x - rect.left - 40;
      const circleY = y - rect.top - 40;
        
        this.x = circleX;
        this.y = circleY;
    } else {
        this.x = -100;
        this.y = -100;
    }
        },
  }
}
</script>

<style scoped>

.mouse-circle {
  position: fixed;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.071);
  pointer-events: none;
}

.navbar {
  transition: all 0.3s ease-in-out;
}
.fadeIn {
  opacity: 1;
}
.fadeInDown {
  opacity: 1;
  transform: translateY(0);
}
.fixed-top2 {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 9999;
  background: #3264f5;
  background: -moz-linear-gradient(left, #7004bc 2%, #3264f5 82%);
  background: -webkit-linear-gradient(left, #7004bc 2%, #3264f5 82%);
  background: linear-gradient(to right, #7004bc 2%, #3264f5 82%);
  margin: 0;
  box-shadow: 0 10px 10px -10px rgba(0, 0, 0, 0.35);
  animation: slideDown 0.9s forwards;
}

@keyframes slideDown {
  from {
    top: -100px;
  }
  to {
    top: 0;
  }
}


.sottolineato {
  position: relative;
}

.sottolineato::before {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 2px;
  background-color: white;
  transform: scaleX(0);
  transition: all 0.4s;
}

.sottolineato:hover::before {
  transform: scaleX(1);
}

.fixed-top {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 200;
  background: #3264f5;
  background: -moz-linear-gradient(left, #3264f5 2%, #7004bc 82%);
  background: -webkit-linear-gradient(left, #3264f5 2%, #7004bc 82%);
  background: linear-gradient(to right, #3264f5 2%, #7004bc 82%);
}

.navbar,
.navbar a {
  font-family: 'Montserrat', sans-serif;
  z-index: 2;
  color: white;
  font-size: 14px;
  font-weight: 500;
}

.navbar img {
  width: 150px;
}

.navbar i {
  font-size: 16px;
}

a {
  display: inline-block;
}

.my-btn {
  --c: white;
  color: var(--c);
  background-color: transparent;
  font-size: 12px;
}

.my-btn:hover {
  color: black;
}

.wrapper-menu {
  width: 25px;
  height: 25px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  cursor: pointer;
  transition: transform 330ms ease-out;
}

.wrapper-menu.open {
  transform: rotate(-45deg);
}

.line-menu {
  background-color: #fff;
  border-radius: 5px;
  width: 100%;
  height: 2px;
}

.line-menu.half {
  width: 50%;
}

.line-menu.start {
  transition: transform 330ms cubic-bezier(0.54, -0.81, 0.57, 0.57);
  transform-origin: right;
}

.open .line-menu.start {
  transform: rotate(-90deg) translateX(3px);
}

.line-menu.end {
  align-self: flex-end;
  transition: transform 330ms cubic-bezier(0.54, -0.81, 0.57, 0.57);
  transform-origin: left;
}

.open .line-menu.end {
  transform: rotate(-90deg) translateX(-3px);
}

.form-control {
  border-radius: 0;
  box-shadow: none;
  border: solid #d4d4d4;
  border-width: 0 0 1px 0;
  margin: 0 auto;
  padding: 10px;
  color: #d4d4d4;
  font-size: 14px;
  font-weight: 300;
  letter-spacing: 1px;
}

.form-control:focus {
  box-shadow: none;
  border-color: #d4d4d4;
}

.form-check {
  margin-top: 50px;
}

.form-check-label {
  color: #7c7c7c;
  font-size: 14px;
  font-weight: 400;
  letter-spacing: 1px;
  margin-left: 10px;
}

.form-check-input {
  border-radius: 0;
  width: 25px;
  height: 25px;
}

.form-check-input:checked {
  background-color: #00BCD4;
  border-color: #00BCD4;
}

.my-btn2 {
  --c: #F023B5;
  color: white;
  background-color: #00A8F5;
  font-size: 14px;
  border: 2px solid #00A8F5;
  border-radius: 50px;
  font-family: "Montserrat", sans-serif;
  text-align: center;
  position: relative;
  overflow: hidden;
  z-index: 2;
  transition: 0.5s;
  font-weight: 700;
  margin-bottom: -100px;
  padding: 9px 34px;
}

.my-btn2:hover {
  color: white;
  background-color: transparent;
  border-color: #F023B5;
  cursor: pointer;
}

.my-btn2 span {
    position: absolute;
    width: 25%;
    height: 100%;
    background-color: var(--c);
    transform: translateY(150%);
    border-radius: 50%;
    left: calc((var(--n) - 1) * 25%);
    transition: 0.5s;
    transition-delay: calc((var(--n) - 1) * 0.1s);
    z-index: -1;
}

.my-btn2:hover span {
  transform: translateY(0) scale(2);
}

.my-btn2 span:nth-child(1) {
  --n: 1;
}

.my-btn2 span:nth-child(2) {
  --n: 2;
}

.my-btn2 span:nth-child(3) {
  --n: 3;
}

.my-btn2 span:nth-child(4) {
  --n: 4;
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

h2 span {
  color: #00A8F5;
  font-weight: 600;
}

.fa-brands {
  width: 40px;
  height: 40px;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  transition: .5s;
}

.fa-brands:hover {
  color: #7004bc;
  background-color: white;
  cursor: pointer;
  box-shadow: 0 0 5px #0c0c0c69;
  text-shadow: 0 0 5px #6f04bc69;
}


</style>
