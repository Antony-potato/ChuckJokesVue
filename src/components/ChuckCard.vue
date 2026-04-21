<script setup>
defineProps({
  icon_url: {
    type: String,
    required: true
  },
  value: {
    type: String,
    required: true
  }
});
</script>

<template>
  <div class="col">
    <div class="card h-100 shadow-sm border-0 custom-card">
      <div class="card-img-wrapper d-flex justify-content-center align-items-center p-4">
        <img :src="icon_url" class="card-img-top chuck-thumbnail" alt="Chuck Norris Icon">
      </div>
      <div class="card-body d-flex flex-column text-center">
        <p class="card-text joke-text flex-grow-1">"{{ value }}"</p>
        <div class="mt-auto">
          <span class="badge rounded-pill bg-dark py-2 px-3">Official Fact</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.custom-card {
  transition: transform 0.3s ease, shadow 0.3s ease;
  background: var(--card-bg, #ffffff);
  border-radius: 1.25rem;
  overflow: hidden;
}

.custom-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.1) !important;
}

.card-img-wrapper {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  border-bottom: 1px solid rgba(0,0,0,0.05);
}

.chuck-thumbnail {
  width: 80px;
  height: 80px;
  object-fit: contain;
  filter: drop-shadow(0 4px 6px rgba(0,0,0,0.1));
}

.joke-text {
  font-size: 1.1rem;
  font-weight: 500;
  color: #2d3436;
  line-height: 1.6;
  padding: 1rem 0;
}

.badge {
  font-weight: 400;
  letter-spacing: 0.5px;
  font-size: 0.8rem;
  text-transform: uppercase;
}
</style>
