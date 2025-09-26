<template>
  <div class="about-page">

    <!-- Hero / Banner -->
    <section class="about-hero">
      <div class="overlay"></div>
      <div class="hero-content">
        <h1>About CHCC</h1>
        <p>Learn who we are, our values, mission, and vision. Discover CHCC’s legacy of excellence in education, service, and community.</p>
      </div>
    </section>

    <!-- Our Mission, Vision, Values -->
    <section class="mission-vision-values">
      <div class="container">
        <div class="mvv-item">
          <h2>Our Mission</h2>
          <p>To deliver transformative education rooted in faith, excellence, and service, shaping minds and hearts for a better tomorrow.</p>
        </div>
        <div class="mvv-item">
          <h2>Vision</h2>
          <p>To be recognized as a leading college committed to holistic formation, academic excellence, and uplifting community lives through faith-inspired leadership.</p>
        </div>
        <div class="mvv-item">
          <h2>Core Values</h2>
          <ul>
            <li>Faith</li>
            <li>Service</li>
            <li>Excellence</li>
            <li>Integrity</li>
            <li>Compassion</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- History / Timeline -->
    <section class="history-section">
      <div class="container">
        <h2>Our Story</h2>
        <div class="timeline">
          <div class="timeline-item" v-for="(event, index) in historyEvents" :key="index">
            <div class="timeline-date">{{ event.year }}</div>
            <div class="timeline-content">
              <h3>{{ event.title }}</h3>
              <p>{{ event.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Why Choose Us / What Makes Us Unique -->
    <section class="why-us">
      <div class="container">
        <h2>Why Choose CHCC?</h2>
        <div class="features">
          <div class="feature" v-for="(f, i) in features" :key="i">
            <i :class="f.icon"></i>
            <h3>{{ f.title }}</h3>
            <p>{{ f.text }}</p>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<script setup>
import { ref } from 'vue'

const historyEvents = ref([
  { year: '1990', title: 'Founded', description: 'Christian Heritage College was established to serve the community with quality education.' },
  { year: '2000', title: 'First Graduation', description: 'We celebrated our first batch of graduates who have gone on to make significant contributions.' },
  { year: '2010', title: 'New Campus Facility', description: 'Opened upgraded facilities including library, labs, and sports grounds.' },
  { year: '2020', title: 'Digital Transition', description: 'Upgraded curriculum to integrate digital learning and online platforms.' }
])

const features = ref([
  { icon: 'pi pi-book', title: 'Comprehensive Academics', text: 'Strong curriculum across arts, sciences, and professional courses.' },
  { icon: 'pi pi-users', title: 'Dedicated Faculty', text: 'Experienced faculty committed to mentoring and excellence.' },
  { icon: 'pi pi-globe', title: 'Global Perspective', text: 'Programs designed to prepare students for a connected world.' }
])
</script>

<style scoped>
.about-page {
  display: flex;
  flex-direction: column;
  gap: 4rem;
}

/* Hero / Banner */
.about-hero {
  position: relative;
  height: 320px;
  background: url('../assets/img/images/banner.jpg') center/cover no-repeat;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
}

.about-hero .overlay {
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.4);
}

.about-hero .hero-content {
  position: relative;
  text-align: center;
  max-width: 800px;
}

.about-hero h1 {
  font-size: 2.8rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.about-hero p {
  font-size: 1.2rem;
}

/* Mission / Vision / Values */
.mission-vision-values .container {
  max-width: 1000px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  text-align: center;
}

.mvv-item h2 {
  font-size: 1.5rem;
  color: #1e3a8a;
  margin-bottom: 0.75rem;
}

.mvv-item p, .mvv-item ul {
  font-size: 1rem;
  color: #374151;
}

.mvv-item ul {
  list-style: none;
  padding-left: 0;
}

.mvv-item ul li {
  margin-bottom: 0.5rem;
}

/* History Timeline */
.history-section .container {
  max-width: 800px;
  margin: 0 auto;
}

.history-section h2 {
  font-size: 1.8rem;
  color: #1e3a8a;
  text-align: center;
  margin-bottom: 2rem;
}

.timeline {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.timeline-item {
  display: grid;
  grid-template-columns: 1fr 3fr;
  gap: 1rem;
  align-items: start;
}

.timeline-date {
  font-weight: bold;
  font-size: 1.25rem;
  color: #f59e0b;
}

.timeline-content h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  color: #1e3a8a;
}

.timeline-content p {
  color: #374151;
}

/* Why Us / Unique Features */
.why-us .container {
  max-width: 1000px;
  margin: 0 auto;
  text-align: center;
}

.why-us h2 {
  font-size: 1.8rem;
  color: #1e3a8a;
  margin-bottom: 2rem;
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 2rem;
}

.feature {
  padding: 1.5rem;
  background: white;
  border: 1px solid #e5e7eb;
  border-radius: 12px;
  transition: transform 0.2s, box-shadow 0.2s;
}

.feature:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
}

.feature i {
  font-size: 2.2rem;
  color: #f59e0b;
  margin-bottom: 1rem;
}

.feature h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  color: #1e3a8a;
}

.feature p {
  color: #374151;
  font-size: 1rem;
}
</style>
