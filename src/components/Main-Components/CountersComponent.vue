<template>
    <div id="counters" class="gradient-bg2">
        <div class="container">
            <div class="row">
                <div class="col-lg-6">
                    <img class="img-fluid" src="@/assets/img3.png" alt="busta">
                </div>
                <div class="col-lg-6 ps-4">
                    <span class="pre-title">We are megaone company</span> 
                        <h2>We have done some great <span class="rotation-word">stuff</span>.</h2>
                        <p class="text-start">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected.</p>
                        <ul class="counter-list">
                            <li class="counter-item me-5 d-flex flex-column"><i class="fa-solid fa-users"></i><span id="value1">{{ primoNumero }} +</span><p>Happy Clients</p></li>
                            <li class="counter-item mx-5 d-flex flex-column"><i class="fa-solid fa-table-list"></i><span id="value2">{{ secondoNumero }} +</span><p>Lines Of Code</p></li>
                            <li class="counter-item ms-5 d-flex flex-column"><i class="fa-solid fa-award"></i><span id="value3">{{ terzoNumero }} +</span><p>Project Completed</p></li>
                        </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CountersComponent',
    data() {
    return {
      primoNumero: 0,
      secondoNumero: 600,
      terzoNumero: 100,
      contatoreAvviato: false,
    };
 },
 mounted() {
    window.addEventListener('scroll', this.controllaScroll);
 },
 beforeUnmount() {
    window.removeEventListener('scroll', this.controllaScroll);
 },
 methods: {
    controllaScroll() {
      if (!this.contatoreAvviato && window.scrollY >= 200) {
        this.avviaContatore();
        this.contatoreAvviato = true; 
      }
    },
    avviaContatore() {
      const incrementoPrimo = setInterval(() => {
        if (this.primoNumero < 500) {
          this.primoNumero++;
        } else {
          clearInterval(incrementoPrimo);
        }
      }, 5); // tempo in millisecondi 0.0005s

      const incrementoSecondo = setInterval(() => {
        if (this.secondoNumero < 1074) {
          this.secondoNumero++;
        } else {
          clearInterval(incrementoSecondo);
        }
      }, 5);

      const incrementoTerzo = setInterval(() => {
        if (this.terzoNumero < 600) {
          this.terzoNumero++;
        } else {
          clearInterval(incrementoTerzo);
        }
      }, 5);
    },
  }
}
</script>

<style scoped>

#counters {
    padding: 100px 0;
    color: white;
}

#counters h2 {
    font-size: 40px;
    font-weight: 600;
    margin-top: 20px;
}

#counters i {
    font-size: 35px;
    margin-bottom: 10px;
}

#counters .counter-item span {
    font-size: 32px;
    font-weight: 500;
    font-family: "Montserrat", sans-serif;
}

.text-start {
    font-weight: 300;
    line-height: 1.8;
    margin-bottom: 30px;
}

.counter-list {
    list-style: none;
    display: flex;
    align-items: center;
    padding-left: 0;

}

.gradient-bg2 {
    background: #237afe;
    background: -moz-linear-gradient(left, #237afe 2%, #03a9f5 82%);
    background: -webkit-linear-gradient(left, #237afe 2%, #03a9f5 82%);
    background: linear-gradient(to right, #237afe 2%, #03a9f5 82%);
}

h2 {
    width: 500px;
    margin-bottom: 30px;
}

.rotation-word {
    font-weight: 600;
}

</style>