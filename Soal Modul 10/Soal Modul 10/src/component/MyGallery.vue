<template>
  <div class="row g-4">
    <div v-for="image in images" :key="image.src" class="col-sm-6 col-lg-4">
      <button
        type="button"
        class="gallery-image-button"
        :aria-label="`Perbesar ${image.alt}`"
        @click="openModal(image)"
      >
        <img :src="image.src" :alt="image.alt" class="img-fluid gallery-image" loading="lazy" />
      </button>
    </div>

    <div
      id="galleryModal"
      ref="galleryModal"
      class="modal fade"
      tabindex="-1"
      aria-labelledby="galleryModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h2 id="galleryModalLabel" class="modal-title fs-5">{{ selectedImage.alt }}</h2>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Tutup"></button>
          </div>
          <div class="modal-body">
            <img :src="selectedImage.src" :alt="selectedImage.alt" class="img-fluid" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Modal } from "bootstrap";
import weeklyRecapOctober from "../assets/Coucou weekly recap 2026-10-12.png";
import weeklyRecapNovember from "../assets/Coucou weekly recap 2026-11-02.png";
import activityScreenshot from "../assets/Screenshot From 2026-11-07 01-10-18.png";

export default {
  data() {
    return {
      images: [
        { src: weeklyRecapOctober, alt: "Coucou weekly recap 12 Oktober 2026" },
        { src: weeklyRecapNovember, alt: "Coucou weekly recap 2 November 2026" },
        { src: activityScreenshot, alt: "Dokumentasi kegiatan 7 November 2026" },
      ],
      selectedImage: { src: "", alt: "" },
      modal: null,
    };
  },
  mounted() {
    this.modal = new Modal(this.$refs.galleryModal);
  },
  beforeUnmount() {
    this.modal?.dispose();
  },
  methods: {
    openModal(image) {
      this.selectedImage = image;
      this.modal.show();
    }
  },
};
</script>

<style scoped>
.gallery-image-button {
  display: block;
  width: 100%;
  padding: 0;
  border: 1px solid #e8e7e4;
  background: #f7f7f6;
}

.gallery-image {
  display: block;
  width: 100%;
  height: 260px;
  object-fit: contain;
}
</style>