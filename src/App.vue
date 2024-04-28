<template>
  <div>
    <NavbarComponent />
    <ModalComponent />
    <JumbtronComponent />
    <AboutUsComponent />
    <ServicesComponent />
    <CountersComponent />
    <TeamComponent />
    <CentralComponent />
    <PortfolioComponent />
    <ClientsComponent />
    <OurBlogComponent />
    <SponsorComponent />
    <LocationComponent />
    <ContactComponent />
    <FooterComponent />
  </div>
  
</template>

<script>
import NavbarComponent from './components/Header-Components/NavbarComponent.vue';
import ModalComponent from './components/Header-Components/ModalComponent.vue';
import JumbtronComponent from './components/Header-Components/JumbtronComponent.vue';
import AboutUsComponent from './components/Main-Components/AboutUsComponent.vue';
import ServicesComponent from './components/Main-Components/ServicesComponent.vue';
import CountersComponent from './components/Main-Components/CountersComponent.vue';
import TeamComponent from './components/Main-Components/TeamComponent.vue';
import CentralComponent from './components/Main-Components/CentralComponent.vue';
import PortfolioComponent from './components/Main-Components/PortfolioComponent.vue';
import ClientsComponent from './components/Main-Components/ClientsComponent.vue';
import OurBlogComponent from './components/Main-Components/OurBlogComponent.vue';
import SponsorComponent from './components/Main-Components/SponsorComponent.vue';
import LocationComponent from './components/Main-Components/LocationComponent.vue';
import ContactComponent from './components/Footer-Components/ContactComponent.vue';
import FooterComponent from './components/Footer-Components/FooterComponent.vue';

export default {
  components: {
    NavbarComponent,
    ModalComponent,
    JumbtronComponent,
    AboutUsComponent,
    ServicesComponent,
    CountersComponent,
    TeamComponent,
    CentralComponent,
    PortfolioComponent,
    ClientsComponent,
    OurBlogComponent,
    SponsorComponent,
    LocationComponent,
    ContactComponent,
    FooterComponent
  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container .row {
  padding: 0 70px;
}

h2, h4, h5, h6 {
  font-family: "Montserrat", sans-serif;
}

p, .pre-title {
  font-family: "Roboto", sans-serif;
}

</style>
