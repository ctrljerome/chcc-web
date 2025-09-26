<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-content">
        <h1>Welcome to CHCC</h1>
        <p>Shaping minds, building futures. Discover our programs, admissions, and vibrant campus life.</p>
        <div class="hero-buttons">
          <router-link to="/admissions" class="btn-primary">Apply Now</router-link>
          <router-link to="/about" class="btn-secondary">Learn More</router-link>
        </div>
      </div>
      <div class="hero-image">
        <img src="../assets/img/images/banner.jpg" alt="Campus Image" />
      </div>
    </section>

    <!-- Quick Links Section -->
    <section class="quick-links">
      <h2>Explore CHCC</h2>
      <div class="cards">
        <router-link to="/programs" class="card">
          <i class="pi pi-book"></i>
          <h3>Programs</h3>
          <p>Browse our academic offerings.</p>
        </router-link>
        <router-link to="/news" class="card">
          <i class="pi pi-megaphone"></i>
          <h3>News & Events</h3>
          <p>Stay updated with campus life.</p>
        </router-link>
        <router-link to="/contact" class="card">
          <i class="pi pi-envelope"></i>
          <h3>Contact Us</h3>
          <p>Get in touch with CHCC.</p>
        </router-link>
      </div>
    </section>

    <!-- Call to Action Section -->
    <section class="cta">
      <h2>Ready to Start Your Journey?</h2>
      <p>Join CHCC and be part of a community committed to excellence.</p>
      <router-link to="/admissions" class="btn-primary">Start Application</router-link>
    </section>
  </div>
</template>

<script setup>
</script>

<style scoped>
/* Hero Section */
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 4rem 2rem;
  background: linear-gradient(135deg, #f9fafb, #eef2ff);
  gap: 2rem;
}

.hero-content {
  flex: 1;
  max-width: 500px;
}

.hero-content h1 {
  font-size: 2.5rem;
  font-weight: 800;
  color: #1e3a8a;
  margin-bottom: 1rem;
}

.hero-content p {
  font-size: 1.1rem;
  color: #374151;
  margin-bottom: 1.5rem;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.btn-primary,
.btn-secondary {
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  font-weight: 600;
  text-decoration: none;
  font-size: 1rem;
  transition: all 0.3s ease;
}

.btn-primary {
  background: #f59e0b;
  color: white;
}

.btn-primary:hover {
  background: #d97706;
}

.btn-secondary {
  background: white;
  border: 1px solid #d1d5db;
  color: #374151;
}

.btn-secondary:hover {
  background: #f9fafb;
}

.hero-image img {
  width: 100%;
  max-width: 450px;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

/* Quick Links */
.quick-links {
  padding: 3rem 2rem;
  text-align: center;
  background: #f9fafb;
}

.quick-links h2 {
  font-size: 1.8rem;
  margin-bottom: 2rem;
  color: #1e3a8a;
}

.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.card {
  background: white;
  border: 1px solid #e5e7eb;
  padding: 2rem 1rem;
  border-radius: 12px;
  text-decoration: none;
  color: #374151;
  transition: transform 0.2s, box-shadow 0.2s;
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

.card i {
  font-size: 2rem;
  color: #f59e0b;
  margin-bottom: 1rem;
}

.card h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  color: #1e3a8a;
}

/* CTA */
.cta {
  text-align: center;
  padding: 4rem 2rem;
  background: linear-gradient(135deg, #1e3a8a, #3b82f6);
  color: white;
}

.cta h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.cta p {
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
}
</style>
