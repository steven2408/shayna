<template>
  <div class="home">
    <HeaderShayna />
    <sectionHero />
    <bannerSection />
    <insta />
    <logo />
    <footerShayna />
  </div>
</template>

<script>
  import HeaderShayna from '@/components/headerShayna.vue'; 
  import sectionHero from '@/components/sectionHero';
  import bannerSection from '@/components/bannerSection';
  import insta from '@/components/insta';
  import logo from '@/components/logo';
  import footerShayna from '@/components/footerShayna';

  export default {
    name: "Home",
    components: {
      HeaderShayna,
      sectionHero,
      bannerSection,
      insta,
      logo,
      footerShayna
    }
  }
</script>
