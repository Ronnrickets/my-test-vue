<template>
  <v-app id="home" class="app-bg">
    
    <SiteHeader/>

    <v-container fluid>
      <!-- <HeroSection/>
      <AboutSection/>
      <ProjectSection/>
      <TestimonialSection/>
      <ContactSection/>
      <CertificateSection/> -->
      <BodySection/>
    </v-container>

    <!-- <SiteFooter/> -->
  </v-app>
</template>

<script>
  import SiteHeader from '../components/SiteHeader';
  import BodySection from '../components/sections/BodySection.vue';
  // import HeroSection from '../components/sections/HeroSection';
  // import AboutSection from '../components/sections/AboutSection';
  // import ProjectSection from '../components/sections/ProjectSection';
  // import TestimonialSection from '../components/sections/TestimonialSection';
  // import ContactSection from '../components/sections/ContactSection';
  // import CertificateSection from '../components/sections/CertificateSection';
  // import SiteFooter from '../components/SiteFooter';
  // import UsersLogin from '../components/UsersLogin.vue';

  export default {
    name: 'HomeView',

    components: {
      SiteHeader,
      BodySection,
      // HeroSection,
      // AboutSection,
      // ProjectSection,
      // TestimonialSection,
      // ContactSection,
      // CertificateSection,
      // SiteFooter,
      // UsersLogin    
    },
  }
</script>

<style scoped>
  .app-bg {
    background-image: url('/public/images/pray.jpg');
    background-size: cover;
    background-position: center;
  }
</style>