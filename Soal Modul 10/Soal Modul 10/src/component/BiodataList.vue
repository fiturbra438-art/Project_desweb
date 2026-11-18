<template>
  <section id="biodata" class="container content-section">
    <div class="section-heading">
      <h2>Biodata</h2>
    </div>
    <dl class="biodata-list mb-0">
      <div v-for="item in biodata" :key="item.label" class="biodata-row">
        <dt>{{ item.label }}</dt>
        <dd>{{ item.value }}</dd>
      </div>
    </dl>
  </section>
</template>

<script>
export default {
  data() {
    return {
      biodata: [
        { label: "Nama", value: "Bryan Fitur Ayni" },
        { label: "NIM", value: "11241020" },
        { label: "Tempat, tanggal lahir", value: "Trenggalek, 12 Juni 2006" },
        { label: "Alamat", value: "Jl. Loa Mali RT 02" },
        { label: "Pekerjaan", value: "Mahasiswa Informatika" },
        { label: "Hobi", value: "Bermain Valorant, makan, dan basket" },
      ],
    };
  },
};
</script>

<style scoped>
.biodata-row {
  display: grid;
  grid-template-columns: minmax(9rem, 0.35fr) 1fr;
  gap: 1rem;
  padding: 0.9rem 0;
  border-bottom: 1px solid #e8e7e4;
}

.biodata-row:first-child {
  border-top: 1px solid #e8e7e4;
}

.biodata-row dt {
  color: #65666a;
  font-weight: 500;
}

.biodata-row dd {
  margin: 0;
}

@media (max-width: 480px) {
  .biodata-row {
    grid-template-columns: 1fr;
    gap: 0.25rem;
  }
}
</style>
