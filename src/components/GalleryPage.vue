<template>
  <div class="gallery">
    <div class="d-flex justify-content-between align-items-center mb-4 pb-2 border-bottom">
      <div>
        <h1 class="h2 font-weight-bold text-primary">{{ title }}</h1>
        <p class="text-muted mb-0">Selected projects shown below are simply examples for website demonstration and not actual projects done.</p>
      </div>
      <div class="badge badge-pill badge-primary p-2">
        {{ items.length }} Featured Projects
      </div>
    </div>

    <!-- Category Filter Chips -->
    <div class="btn-group mb-4" role="group">
      <button
        type="button"
        class="btn btn-sm"
        :class="selectedCategory === 'all' ? 'btn-primary' : 'btn-outline-secondary'"
        @click="selectedCategory = 'all'">
        All Works
      </button>
      <button
        type="button"
        class="btn btn-sm"
        :class="selectedCategory === 'web' ? 'btn-primary' : 'btn-outline-secondary'"
        @click="selectedCategory = 'web'">
        Web Apps
      </button>
      <button
        type="button"
        class="btn btn-sm"
        :class="selectedCategory === 'ui' ? 'btn-primary' : 'btn-outline-secondary'"
        @click="selectedCategory = 'ui'">
        UI / UX
      </button>
    </div>

    <!-- Gallery Grid -->
    <div class="row">
      <div class="col-lg-4 col-md-6 mb-4" v-for="item in filteredItems" :key="item.id">
        <div class="card h-100 shadow-sm border-0 overflow-hidden">
          <div class="gallery-image-wrapper bg-light d-flex align-items-center justify-content-center" :style="{ backgroundColor: item.bg }">
            <span class="display-4">{{ item.icon }}</span>
          </div>
          <div class="card-body">
            <span class="badge badge-secondary mb-2">{{ item.category.toUpperCase() }}</span>
            <h5 class="card-title font-weight-bold">{{ item.name }}</h5>
            <p class="card-text text-muted small">{{ item.description }}</p>
          </div>
          <div class="card-footer bg-white border-0 pt-0">
            <small class="text-primary font-weight-bold">View Case Study &rarr;</small>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GalleryPage',
  data () {
    return {
      title: 'Selected Work',
      selectedCategory: 'all',
      items: [
        { id: 1, name: 'Personal Portfolio Website', category: 'web', icon: '🧭', bg: '#111123', description: 'Multi-page single page application built with Vue 3, Vue Router, and Vite.' },
        { id: 2, name: 'Responsive Dashboard UI', category: 'ui', icon: '📊', bg: '#f1edc0', description: 'Admin analytics console with clean charts, data tables, and a mobile-first layout.' },
        { id: 3, name: 'Cloud Deployment Setup', category: 'web', icon: '☁️', bg: '#111123', description: 'Automated deployment workflow to Vercel and Netlify with SPA route fallbacks.' },
        { id: 4, name: 'E-Commerce Storefront', category: 'web', icon: '🛒', bg: '#f1edc0', description: 'Shopping cart with state management, product filters, and a streamlined checkout flow.' },
        { id: 5, name: 'Mobile Design System', category: 'ui', icon: '📱', bg: '#111123', description: 'Cross-platform typography, icon sets, and accessible color tokens.' },
        { id: 6, name: 'REST API Integration', category: 'web', icon: '⚡', bg: '#f1edc0', description: 'Asynchronous Axios requests communicating with an Express backend.' }
      ]
    }
  },
  computed: {
    filteredItems () {
      if (this.selectedCategory === 'all') return this.items
      return this.items.filter(item => item.category === this.selectedCategory)
    }
  }
}
</script>

<style scoped>
.gallery-image-wrapper {
  height: 180px;
}
.card {
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}
.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 24px rgba(0,0,0,0.1) !important;
}
</style>
