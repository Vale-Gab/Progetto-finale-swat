<template>
  <div id="portfolio">
    <div class="container">
      <div class="row">
        <div class="col-md-12 text-center">
          <span class="pre-title">We are megaone company</span>
          <h2>We have <span class="rotation-word">designed</span> some great projects</h2>
          <p class="post-title">
            There are many variations of passages of Lorem Ipsum available, but the majority have
            suffered alteration in some form, by injected.
          </p>
        </div>
      </div>
      <div class="row">
        <div class="cbp-l-filters-button text-center d-flex justify-content-center gallery-menu" id="menu-portfolio">
          <a class="cbp-filter-item cbp-filter-item-active"
            data-filter="*"
            @click="filterImages('all')" :class="{ active: currentCategory === 'all' }"
            >All</a>
          <span class="text-blue">/</span>
          <a class="cbp-filter-item" data-filter=".graphic" @click="filterImages('graphic')" :class="{ active: currentCategory === 'graphic' }"
            >Graphic Design</a>
          <span class="text-blue">/</span>
          <a class="cbp-filter-item" data-filter=".web-design" @click="filterImages('web-design')" :class="{ active: currentCategory === 'web-design' }"
            >Web design</a>
          <span class="text-blue">/</span>
          <a class="cbp-filter-item" data-filter=".graphic" @click="filterImages('seo')" :class="{ active: currentCategory === 'seo' }">SEO</a>
          <span class="text-blue">/</span>
          <a class="cbp-filter-item" data-filter=".marketing" @click="filterImages('marketing')" :class="{ active: currentCategory === 'marketing' }"
            >Marketing</a>
        </div>
        <div class="grid-container justify-content-center">
          <div
            v-for="(image, index) in images"
            :key="index"
            :class="'image-' + index"
            class="image-container">
            <img
              class="image"
              :src="image.src"
              :alt="image.alt"
              :class="image.category"
              v-show="showImage(image.category)"
            />
            <div class="overlay" @click="openModal(index)">
              <div class="piu"></div>
              <h5 class="text">Latest Work</h5>
              <p class="text-par">See Our Amazing Work</p>
            </div>
          </div>
          <div v-if="showModal" class="modal" tabindex="-1" role="dialog">
            <div class="modal-dialog modal-dialog-centered" role="document">
              <div class="modal-content">
                <div class="modal-header">
                  <div class="w3-text-white w3-xxlarge w3-hover-text-grey w3-container w3-display-topright"
                    @click="closeModal"
                    style="cursor: pointer">
                    <i class="fa-solid fa-xmark"></i>
                  </div>
                </div>
                <div class="modal-body">
                  <div class="w3-display-left w3-btn" @click="plusDivs(-1)">
                    <i class="fa-solid fa-angle-left"></i>
                  </div>
                  <img :src="images[currentIndex].src" class="img-fluid" alt="Modal Image" />
                  <div class="w3-display-right w3-btn" @click="plusDivs(1)">
                    <i class="fa-solid fa-angle-right"></i>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import work1 from '@/assets/work-1.jpg'
import work2 from '@/assets/work-2.jpg'
import work4 from '@/assets/work-3.jpg'
import work3 from '@/assets/work-4.jpg'
import work5 from '@/assets/work-5.jpg'
import work6 from '@/assets/work-6.jpg'
import work7 from '@/assets/work-7.jpg'
import work8 from '@/assets/work-8.jpg'

export default {
  name: 'PortfolioComponent',
  data() {
    return {
      images: [
        { src: work1, alt: 'Lattina', category: 'graphic' },
        { src: work2, alt: 'Immagine Animali 1', category: 'graphic' },
        { src: work3, alt: 'Immagine Animali 2', category: 'web-design' },
        { src: work4, alt: 'Immagine Fiori 2', category: 'web-design' },
        { src: work5, alt: 'Immagine Fiori 3', category: 'seo' },
        { src: work6, alt: 'Immagine Animali3', category: 'seo' },
        { src: work7, alt: 'Immagine Animali3', category: 'marketing' },
        { src: work8, alt: 'Immagine Animali3', category: 'marketing' }
      ],
      currentCategory: 'all',
      showModal: false,
      currentIndex: 0
    }
  },
  methods: {
    filterImages(category) {
      this.currentCategory = category
    },
    showImage(category) {
      return this.currentCategory === 'all' || category === this.currentCategory
    },
    openModal(index) {
      this.showModal = true
      this.currentIndex = index
    },
    closeModal() {
      this.showModal = false
    },
    plusDivs(n) {
      this.currentIndex += n
      if (this.currentIndex >= this.images.length) {
        this.currentIndex = 0
      }
      if (this.currentIndex < 0) {
        this.currentIndex = this.images.length - 1
      }
    },
    currentDiv(n) {
      this.currentIndex = n
    }
  },

  created() {
    this.filterImages('all')
  }
}
</script>

<style scoped>
#portfolio {
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

.post-title {
  color: #696969;
  font-size: 16px;
  font-weight: 300;
  line-height: 1.8;
  width: 500px;
  margin: 25px auto;
}

.cbp-filter-item {
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 500;
  color: #333333;
  margin: 0 15px;
  text-transform: capitalize;
  margin-bottom: 35px;
  text-decoration: none;
}

a:hover {
  color: #00a8f5;
  cursor: pointer;
}

.active {
  color: #f041b4;
}

.cbp-l-filters-button {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  font-weight: 200;
  color: #696969;
}

.grid-container {
  display: grid;
  grid-template-areas:
    'image-0 image-1 image-3 image-3'
    'image-0 image-2 image-3 image-3'
    'image-4 image-4 image-5 image-5'
    'image-4 image-4 image-6 image-7'; /* Definizione delle aree di template */
  grid-gap: none; /* Spazio tra le immagini */
}

.image-container {
  overflow: hidden;
  position: relative; /* Per adattare l'immagine al contenitore */
}

.image-container:hover .overlay {
  opacity: 1; /* Opacità al passaggio del mouse */
}

.image {
  width: 100%;
  height: auto;
  object-fit: cover; /* Per adattare l'immagine al contenitore */
}

/* Assegnazione delle aree di template ai singoli elementi */
.image-0 {
  grid-area: image-0;
}
.image-1 {
  grid-area: image-1;
}
.image-2 {
  grid-area: image-2;
}
.image-3 {
  grid-area: image-3;
}
.image-4 {
  grid-area: image-4;
}
.image-5 {
  grid-area: image-5;
}
.image-6 {
  grid-area: image-6;
}
.image-7 {
  grid-area: image-7;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #00a7f5db;
  opacity: 0;
  transition: 0.5s;
  overflow: hidden;
}

.overlay:hover {
  opacity: 1;
  cursor: pointer;
}

.piu::before {
  content: ' ';
  position: absolute;
  background: #fff;
  width: 2px;
  height: 70px;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.piu::after {
  content: ' ';
  position: absolute;
  background: #fff;
  height: 2px;
  width: 70px;
  margin-top: -1px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

h5 {
  color: white;
  text-align: center;
  font-size: 20px;
  font-weight: 400;
}

p {
  color: white;
  text-align: center;
  font-size: 14px;
  font-weight: 300;
}

.piu {
  vertical-align: middle;
  text-align: center;
  padding: 20px 0;
}

.modal {
  background: rgba(0, 0, 0, 0.731);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-dialog {
  max-width: 90%;
}

.modal-content {
  background-color: transparent;
  border: none;
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.modal-header {
  border-bottom: none;
  display: flex;
  justify-content: end;
  width: 98vw;
  height: 6vw;
  align-items: center;
}

.modal-content i {
  color: rgb(203, 203, 203);
  font-size: 26px;
  border-radius: 50%;
  border-width: 2px;
  border-style: solid;
  border-color: rgb(203, 203, 203);
  height: 40px;
  width: 40px;
  cursor: pointer;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-body {
  min-width: 98vw;
  min-height: 30vh;
  overflow: hidden;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

</style>
