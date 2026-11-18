<template>
  <section id="beranda" class="container profile-intro">
    <div class="row align-items-center g-4 g-lg-5">
      <div class="col-md-5 col-lg-4">
        <img
          class="profile-picture img-fluid"
          :src="profileImage"
          alt="Foto Bryan Fitur Ayni"
        />
      </div>
      <div class="col-md-7 col-lg-8">
        <p class="text-secondary mb-2">Mahasiswa Informatika · NIM 11241020</p>
        <h1 class="profile-name">Bryan Fitur Ayni</h1>
        <p class="profile-summary">
          Saya Fitur dan saya sedang bikin fitur. Senang belajar, berorganisasi,
          dan mencoba hal-hal baru.
        </p>
        <a class="btn btn-outline-dark" href="#biodata">Lihat biodata</a>
      </div>
    </div>
  </section>
</template>

<script>
import profileImage from "../assets/bryan-profile.jpg";

export default {
  data() {
    return { profileImage };
  },
};
</script>

<style scoped>
.profile-intro {
  padding-top: 3rem;
  padding-bottom: 2rem;
}

.profile-picture {
  display: block;
  width: 100%;
  max-height: 390px;
  object-fit: cover;
  object-position: center 35%;
}

.profile-name {
  margin-bottom: 1rem;
  font-size: clamp(2.25rem, 5vw, 4rem);
  font-weight: 650;
  letter-spacing: -0.045em;
}

.profile-summary {
  max-width: 35rem;
  margin-bottom: 1.5rem;
  color: #65666a;
  font-size: 1.1rem;
  line-height: 1.7;
}
</style>