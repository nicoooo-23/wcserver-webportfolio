<template>
  <div class="blog">
    <div class="jumbotron bg-light p-4 rounded mb-4 shadow-sm border">
      <h1 class="display-5 font-weight-bold text-primary">{{ title }}</h1>
      <p class="lead">Notes on what I'm learning, building, and figuring out as a web developer.</p>
    </div>

    <div class="row">
      <div class="col-md-6 mb-4" v-for="post in posts" :key="post.id">
        <div class="card h-100 shadow-sm border-0">
          <div class="card-body">
            <span class="badge badge-info mb-2">{{ post.category }}</span>
            <h5 class="card-title font-weight-bold">{{ post.title }}</h5>
            <p class="card-text text-muted">{{ post.summary }}</p>
          </div>
          <div class="card-footer bg-transparent border-0 d-flex justify-content-between align-items-center text-muted small">
            <span><i class="far fa-calendar-alt mr-1"></i> {{ post.date }}</span>
            <span><i class="far fa-clock mr-1"></i> {{ post.readTime }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlogPage',
  data () {
    return {
      title: 'Blog',
      posts: [
        {
          id: 1,
          category: 'Vue.js',
          title: 'Building My Portfolio as a Vue 3 Single Page App',
          summary: 'How I structured routes, components, and navigation to make a fast, multi-page feel without full page reloads.',
          date: 'Sep 24, 2026',
          readTime: '4 min read'
        },
        {
          id: 2,
          category: 'Tooling',
          title: 'Why I Moved My Projects from Webpack to Vite',
          summary: 'Faster dev server startup, instant hot reloads, and simpler configuration through native ES modules.',
          date: 'Sep 20, 2026',
          readTime: '5 min read'
        },
        {
          id: 3,
          category: 'Deployment',
          title: 'Fixing 404 Errors on Refresh for Hosted SPAs',
          summary: 'A practical walkthrough of rewriting all requests to index.html on Vercel and Netlify so deep links keep working.',
          date: 'Sep 15, 2026',
          readTime: '5 min read'
        }
      ]
    }
  }
}
</script>

<style scoped>
.blog {
  padding-bottom: 20px;
}
.card {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.08) !important;
}
</style>
