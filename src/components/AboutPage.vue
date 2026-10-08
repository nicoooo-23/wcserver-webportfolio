<template>
  <div class="about">
    <!-- Hero Banner -->
    <div class="jumbotron bg-primary text-white p-5 rounded shadow-sm mb-4">
      <h1 class="display-4 font-weight-bold">About Me</h1>
      <p class="lead">Back-End Developer with a focus on Web Systems and Technologies</p>
      <hr class="my-4 bg-white opacity-25">
      <p>I enjoy turning ideas into fast, accessible, and well-structured web experiences, from component-driven interfaces to production deployment.</p>
    </div>

    <div class="row">
      <!-- Student Bio Card -->
      <div class="col-md-6 mb-4">
        <div class="card shadow-sm h-100 border-0">
          <div class="card-header bg-light font-weight-bold">
            <i class="fas fa-user-graduate mr-2 text-primary"></i>Profile
          </div>
          <div class="card-body">
            <h5 class="card-title font-weight-bold">Ella Nicole Rivera</h5>
            <p class="card-text text-muted">Web Systems and Technologies Specialization</p>
            <ul class="list-group list-group-flush mb-3">
              <li class="list-group-item d-flex justify-content-between px-0">
                <span class="text-muted">Focus:</span>
                <strong>Web Development</strong>
              </li>
              <li class="list-group-item d-flex justify-content-between px-0">
                <span class="text-muted">Interests:</span>
                <strong>API Integration and Backend Development</strong>
              </li>
              <li class="list-group-item d-flex justify-content-between px-0">
                <span class="text-muted">Main Stack:</span>
                <strong>Vue.js, JavaScript, Node.js, Express.js</strong>
              </li>
              <li class="list-group-item d-flex justify-content-between px-0">
                <span class="text-muted">Status:</span>
                <span class="badge badge-success">Open to Work</span>
              </li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Tech Stack & Competencies -->
      <div class="col-md-6 mb-4">
        <div class="card shadow-sm h-100 border-0">
          <div class="card-header bg-light font-weight-bold">
            <i class="fas fa-code mr-2 text-primary"></i>Core Competencies
          </div>
          <div class="card-body">
            <div class="mb-3">
              <h6 class="font-weight-bold mb-1">Vue.js &amp; Component Architecture</h6>
              <p class="small text-muted mb-0">Building reusable, maintainable single page applications with Vue 3, Vue Router, and clean component design.</p>
            </div>
            <div class="mb-3">
              <h6 class="font-weight-bold mb-1">Responsive UI Design</h6>
              <p class="small text-muted mb-0">Crafting mobile-friendly layouts with clear typography, consistent spacing, and accessible color choices.</p>
            </div>
            <div class="mb-3">
              <h6 class="font-weight-bold mb-1">Deployment &amp; Hosting</h6>
              <p class="small text-muted mb-0">Shipping optimized production builds to cloud platforms with proper routing and server rewrite configuration.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>

<style scoped>
.about {
  padding-bottom: 20px;
}
</style>
