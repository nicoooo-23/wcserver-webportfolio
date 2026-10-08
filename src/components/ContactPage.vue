<template>
  <div class="contact">
    <div class="row">
      <div class="col-lg-7 mb-4">
        <div class="card shadow-sm border-0">
          <div class="card-body p-4">
            <h2 class="h4 font-weight-bold text-primary mb-3">Get in Touch</h2>
            <p class="text-muted small mb-4">Have a project in mind or want to collaborate? Fill in the details below.</p>

            <div v-if="submitted" class="alert alert-success alert-dismissible fade show" role="alert">
              <strong>Thank you, {{ form.name }}!</strong> Your message has been received, and I'll get back to you soon.
              <button type="button" class="close" @click="submitted = false">&times;</button>
            </div>

            <form @submit.prevent="handleSubmit">
              <div class="form-group mb-3">
                <label class="font-weight-bold small">Full Name</label>
                <input type="text" class="form-control" v-model="form.name" placeholder="John Doe" required>
              </div>

              <div class="form-group mb-3">
                <label class="font-weight-bold small">Email Address</label>
                <input type="email" class="form-control" v-model="form.email" placeholder="you@example.com" required>
              </div>

              <div class="form-group mb-3">
                <label class="font-weight-bold small">Subject</label>
                <select class="form-control" v-model="form.subject">
                  <option>Project Inquiry</option>
                  <option>Collaboration</option>
                  <option>Job Opportunity</option>
                </select>
              </div>

              <div class="form-group mb-4">
                <label class="font-weight-bold small">Message</label>
                <textarea class="form-control" rows="4" v-model="form.message" placeholder="Type your message here..." required></textarea>
              </div>

              <button type="submit" class="btn btn-primary font-weight-bold px-4">
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>

      <!-- Contact Info Sidebar -->
      <div class="col-lg-5 mb-4">
        <div class="card shadow-sm border-0 bg-light h-100">
          <div class="card-body p-4">
            <h3 class="h5 font-weight-bold mb-3">Contact Details</h3>
            <p class="text-muted small mb-4">Reach out through the form or any of the channels below. I usually reply within a couple of days.</p>

            <div class="d-flex mb-3">
              <div class="mr-3 text-primary"><i class="fas fa-map-marker-alt fa-lg"></i></div>
              <div>
                <strong class="d-block small">Work Setup:</strong>
                <span class="text-muted small">Remote-friendly</span>
              </div>
            </div>

            <div class="d-flex mb-3">
              <div class="mr-3 text-primary"><i class="fas fa-envelope fa-lg"></i></div>
              <div>
                <strong class="d-block small">Email:</strong>
                <span class="text-muted small">riveraent05@proton.me</span>
              </div>
            </div>

            <div class="d-flex">
              <div class="mr-3 text-primary"><i class="fas fa-clock fa-lg"></i></div>
              <div>
                <strong class="d-block small">Availability:</strong>
                <span class="text-muted small">Mon - Fri: 9:00 AM - 5:00 PM</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage',
  data () {
    return {
      submitted: false,
      form: {
        name: '',
        email: '',
        subject: 'Project Inquiry',
        message: ''
      }
    }
  },
  methods: {
    handleSubmit () {
      this.submitted = true
      // Form submitted state handled
    }
  }
}
</script>

<style scoped>
.contact {
  padding-bottom: 20px;
}
</style>
