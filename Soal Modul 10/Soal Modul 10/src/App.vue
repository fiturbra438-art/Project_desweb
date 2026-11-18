<template>
  <div>
    <HeaderNavbar />
    <main>
      <HeroProfile />
      <BiodataList />
      <section id="pengalaman" class="container content-section">
        <div class="section-heading d-flex flex-column flex-md-row justify-content-between align-items-md-end gap-2">
          <h2>Pengalaman</h2>
          <p class="mb-0 text-secondary">Organisasi dan kegiatan</p>
        </div>
        <ExperienceList />
      </section>
      <section id="galeri" class="container content-section">
        <div class="section-heading">
          <h2>Galeri</h2>
        </div>
        <MyGallery />
      </section>
      <section id="kontak" class="container content-section contact-section">
        <div class="section-heading">
          <h2>Kontak</h2>
        </div>
        <ContactForm />
      </section>
    </main>
    <TheFooter />
  </div>
</template>

<script>
import HeaderNavbar from "./component/HeaderNavbar.vue";
import HeroProfile from "./component/HeroProfile.vue";
import BiodataList from "./component/BiodataList.vue";
import ExperienceList from "./component/ExperienceList.vue";
import MyGallery from "./component/MyGallery.vue";
import ContactForm from "./component/ContactForm.vue";
import TheFooter from "./component/TheFooter.vue";

export default {
  components: {
    HeaderNavbar,
    HeroProfile,
    BiodataList,
    ExperienceList,
    MyGallery,
    ContactForm,
    TheFooter,
  },
};
</script>

<style>
:root {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  color: #292a2c;
  background: #fff;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
}

body {
  min-width: 320px;
  margin: 0;
  background: #fff;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 4.5rem;
}

.content-section {
  padding-top: 3rem;
  padding-bottom: 0.5rem;
}

.section-heading {
  margin-bottom: 1.25rem;
  padding-bottom: 0.75rem;
  border-bottom: 1px solid #e8e7e4;
}

.section-heading h2 {
  margin: 0;
  color: #292a2c;
  font-size: 1.5rem;
  font-weight: 650;
}

.contact-section {
  max-width: 760px;
}
</style>