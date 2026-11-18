<template>
  <div class="row g-4">
    <div
      v-for="experience in experiences"
      :key="experience.title"
      class="col-md-6"
    >
      <article class="card h-100 experience-card">
        <div class="card-body">
          <h3 class="card-title">{{ experience.title }}</h3>
          <p class="experience-role mb-2">{{ experience.role }}</p>
          <p class="card-text">{{ experience.description }}</p>
        </div>
      </article>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      experiences: [
        {
          title: "Komting IF24",
          role: "Koordinator kelas",
          year: "",
          description: "Membantu koordinasi komunikasi dan kegiatan bersama teman-teman sekelas.",
        },
        {
          title: "Wakahima",
          role: "Wakil ketua himpunan mahasiswa",
          year: "",
          description: "Berpartisipasi dalam kegiatan dan organisasi kemahasiswaan.",
        },
        {
          title: "Duta Pelajar & Duta Anti Narkoba",
          role: "Duta",
          year: "",
          description: "Pengalaman sebagai duta pelajar dan duta anti narkoba.",
        },
        {
          title: "Wirausaha",
          role: "Usaha mandiri",
          year: "",
          description: "Pernah berjualan plastik dan tahu.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.experience-card {
  border: 1px solid #e8e7e4;
  border-radius: 0.25rem;
}

.card-title {
  color: #292a2c;
  font-size: 1.1rem;
  font-weight: 650;
}

.experience-role {
  color: #65666a;
}

.card-text {
  margin-bottom: 0;
  color: #65666a;
  line-height: 1.6;
}
</style>