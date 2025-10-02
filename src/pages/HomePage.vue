<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-background">
        <div class="hero-overlay"></div>
        <div class="hero-particles"></div>
        <div class="hero-gradient"></div>
      </div>
      
      <div class="hero-container">
        <div class="hero-content">
          <div class="hero-badge">
            <i class="pi pi-star"></i>
            <span>Excellence Since 1990</span>
          </div>
          
          <h1 class="hero-title">
            Welcome to 
            <span class="highlight">CHCC</span>
          </h1>
          
          <p class="hero-subtitle">
            Shaping minds, building futures. Discover our innovative programs, 
            comprehensive admissions process, and vibrant campus life at 
            Concepcion Holy Cross College.
          </p>
          
          <div class="hero-buttons">
            <router-link to="/admissions" class="btn-primary">
              <i class="pi pi-plus"></i>
              <span>Apply Now</span>
            </router-link>
            <router-link to="/about" class="btn-secondary">
              <i class="pi pi-info-circle"></i>
              <span>Learn More</span>
            </router-link>
          </div>
          
          <div class="hero-stats">
            <div class="stat">
              <div class="stat-number">5000+</div>
              <div class="stat-label">Students</div>
            </div>
            <div class="stat">
              <div class="stat-number">50+</div>
              <div class="stat-label">Faculty</div>
            </div>
            <div class="stat">
              <div class="stat-number">20+</div>
              <div class="stat-label">Programs</div>
            </div>
          </div>
        </div>
        
        <div class="hero-visual">
          <div class="hero-image-container">
            <div class="image-backdrop"></div>
            <img src="../assets/img/images/banner.jpg" alt="CHCC Campus" class="hero-image" />
            <div class="floating-elements">
              <div class="floating-card">
                <i class="pi pi-graduation-cap"></i>
                <span>Quality Education</span>
              </div>
              <div class="floating-card">
                <i class="pi pi-users"></i>
                <span>Expert Faculty</span>
              </div>
              <div class="floating-card">
                <i class="pi pi-trophy"></i>
                <span>Excellence Awards</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Quick Access Cards -->
    <section class="quick-access">
      <div class="container">
        <div class="section-header">
          <h2>Explore CHCC</h2>
          <p>Everything you need to know about our college</p>
        </div>
        
        <div class="cards-grid">
          <router-link 
            to="/programs" 
            class="access-card programs"
            v-motion-slide-visible-once-bottom
          >
            <div class="card-icon">
              <i class="pi pi-book"></i>
            </div>
            <div class="card-content">
              <h3>Academic Programs</h3>
              <p>Explore our comprehensive range of undergraduate and graduate programs</p>
              <div class="card-badge">20+ Programs</div>
            </div>
            <div class="card-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </router-link>

          <router-link 
            to="/admissions" 
            class="access-card admissions"
            v-motion-slide-visible-once-bottom
            :style="{ transitionDelay: '100ms' }"
          >
            <div class="card-icon">
              <i class="pi pi-user-plus"></i>
            </div>
            <div class="card-content">
              <h3>Admissions</h3>
              <p>Start your journey with us. Learn about requirements and application process</p>
              <div class="card-badge">Now Open</div>
            </div>
            <div class="card-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </router-link>

          <router-link 
            to="/campus-life" 
            class="access-card campus"
            v-motion-slide-visible-once-bottom
            :style="{ transitionDelay: '200ms' }"
          >
            <div class="card-icon">
              <i class="pi pi-home"></i>
            </div>
            <div class="card-content">
              <h3>Campus Life</h3>
              <p>Discover student organizations, facilities, and campus activities</p>
              <div class="card-badge">Vibrant Community</div>
            </div>
            <div class="card-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </router-link>

          <router-link 
            to="/news" 
            class="access-card news"
            v-motion-slide-visible-once-bottom
            :style="{ transitionDelay: '300ms' }"
          >
            <div class="card-icon">
              <i class="pi pi-megaphone"></i>
            </div>
            <div class="card-content">
              <h3>News & Events</h3>
              <p>Stay updated with the latest campus news, events, and announcements</p>
              <div class="card-badge">Latest Updates</div>
            </div>
            <div class="card-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </router-link>

          <router-link 
            to="/library" 
            class="access-card library"
            v-motion-slide-visible-once-bottom
            :style="{ transitionDelay: '400ms' }"
          >
            <div class="card-icon">
              <i class="pi pi-book-open"></i>
            </div>
            <div class="card-content">
              <h3>Digital Library</h3>
              <p>Access our extensive collection of digital resources and research materials</p>
              <div class="card-badge">24/7 Access</div>
            </div>
            <div class="card-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </router-link>

          <router-link 
            to="/contact" 
            class="access-card contact"
            v-motion-slide-visible-once-bottom
            :style="{ transitionDelay: '500ms' }"
          >
            <div class="card-icon">
              <i class="pi pi-envelope"></i>
            </div>
            <div class="card-content">
              <h3>Contact Us</h3>
              <p>Get in touch with our admissions team and academic advisors</p>
              <div class="card-badge">Quick Response</div>
            </div>
            <div class="card-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </router-link>
        </div>
      </div>
    </section>

    <!-- Features Highlight -->
    <section class="features-section">
      <div class="container">
        <div class="features-content">
          <div class="features-text">
            <div class="section-badge">
              <i class="pi pi-star"></i>
              <span>Why Choose CHCC</span>
            </div>
            <h2>Excellence in Every Aspect</h2>
            <p>
              We provide a holistic educational experience that combines academic rigor 
              with character formation, preparing students for successful careers and 
              meaningful lives.
            </p>
            
            <div class="features-list">
              <div class="feature-item">
                <div class="feature-check">
                  <i class="pi pi-check"></i>
                </div>
                <div class="feature-text">
                  <h4>Accredited Programs</h4>
                  <p>All programs are fully accredited and meet industry standards</p>
                </div>
              </div>
              
              <div class="feature-item">
                <div class="feature-check">
                  <i class="pi pi-check"></i>
                </div>
                <div class="feature-text">
                  <h4>Expert Faculty</h4>
                  <p>Learn from experienced professors and industry professionals</p>
                </div>
              </div>
              
              <div class="feature-item">
                <div class="feature-check">
                  <i class="pi pi-check"></i>
                </div>
                <div class="feature-text">
                  <h4>Modern Facilities</h4>
                  <p>State-of-the-art classrooms, labs, and learning spaces</p>
                </div>
              </div>
            </div>
            
            <router-link to="/about" class="btn-outline">
              Learn More About Us
              <i class="pi pi-arrow-right"></i>
            </router-link>
          </div>
          
          <div class="features-visual">
            <div class="visual-grid">
              <div class="visual-item large">
                <img src="../assets/img/images/campus-1.jpg" alt="Campus View" />
              </div>
              <div class="visual-item">
                <img src="../assets/img/images/students-1.jpg" alt="Students" />
              </div>
              <div class="visual-item">
                <img src="../assets/img/images/facilities-1.jpg" alt="Facilities" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section class="cta-section">
      <div class="cta-background">
        <div class="cta-overlay"></div>
        <div class="cta-pattern"></div>
      </div>
      
      <div class="container">
        <div class="cta-content">
          <div class="cta-badge">
            <i class="pi pi-lightning"></i>
            <span>Ready to Start?</span>
          </div>
          
          <h2>Begin Your Journey with CHCC</h2>
          <p>
            Join thousands of successful graduates who started their careers here. 
            Take the first step towards your bright future today.
          </p>
          
          <div class="cta-buttons">
            <router-link to="/admissions" class="btn-primary large">
              <i class="pi pi-plus"></i>
              <span>Start Application</span>
            </router-link>
            <router-link to="/programs" class="btn-secondary large">
              <i class="pi pi-eye"></i>
              <span>View Programs</span>
            </router-link>
          </div>
          
          <div class="cta-note">
            <i class="pi pi-info-circle"></i>
            <span>Applications for Academic Year 2024-2025 are now open</span>
          </div>
        </div>
      </div>
    </section>

    <!-- News Preview -->
    <section class="news-preview">
      <div class="container">
        <div class="section-header">
          <h2>Latest News & Updates</h2>
          <router-link to="/news" class="view-all-link">
            View All News
            <i class="pi pi-arrow-right"></i>
          </router-link>
        </div>
        
        <div class="news-grid">
          <article 
            class="news-card featured" 
            v-for="(article, index) in featuredNews" 
            :key="index"
          >
            <div class="news-image">
              <img :src="article.image" :alt="article.title" />
              <div class="news-category">{{ article.category }}</div>
            </div>
            <div class="news-content">
              <div class="news-meta">
                <time>{{ article.date }}</time>
                <span class="author">{{ article.author }}</span>
              </div>
              <h3>{{ article.title }}</h3>
              <p>{{ article.excerpt }}</p>
              <router-link :to="`/news/${article.slug}`" class="read-more">
                Read More
                <i class="pi pi-arrow-right"></i>
              </router-link>
            </div>
          </article>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const featuredNews = ref([
  {
    title: 'CHCC Receives Excellence Award in Education',
    excerpt: 'Our college has been recognized for outstanding contribution to higher education in the region.',
    image: '../assets/img/news/award-ceremony.jpg',
    category: 'Achievement',
    date: 'March 10, 2024',
    author: 'Facilities Team',
    slug: 'new-science-laboratory'
  },
  {
    title: 'Student Exchange Program Launched',
    excerpt: 'CHCC partners with international universities to provide global learning opportunities.',
    image: '../assets/img/news/exchange-program.jpg',
    category: 'Programs',
    date: 'March 5, 2024',
    author: 'International Office',
    slug: 'student-exchange-program'
  }
])

// Animation and scroll effects can be added here
onMounted(() => {
  // Add any initialization code here
})
</script>

<style scoped>
:root {
  --primary-color: #1e40af;
  --primary-light: #3b82f6;
  --primary-dark: #1e3a8a;
  --accent-color: #f59e0b;
  --accent-hover: #d97706;
  --success-color: #10b981;
  --text-dark: #1f2937;
  --text-light: #6b7280;
  --text-lighter: #9ca3af;
  --border-color: #e5e7eb;
  --bg-light: #f8fafc;
  --bg-lighter: #f1f5f9;
  --white: #ffffff;
  --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --gradient-primary: linear-gradient(135deg, var(--primary-color), var(--primary-light));
  --gradient-accent: linear-gradient(135deg, var(--accent-color), var(--accent-hover));
}

.home {
  overflow-x: hidden;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

/* Hero Section */
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  overflow: hidden;
}

.hero-background {
  position: absolute;
  inset: 0;
  z-index: -1;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: var(--gradient-primary);
}

.hero-particles {
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle at 25% 25%, rgba(255, 255, 255, 0.1) 2px, transparent 2px);
  background-size: 50px 50px;
  animation: float 20s infinite linear;
}

.hero-gradient {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse at center, transparent 0%, rgba(30, 64, 175, 0.8) 100%);
}

@keyframes float {
  0% { transform: translate(0, 0); }
  100% { transform: translate(-50px, -50px); }
}

.hero-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  min-height: 100vh;
}

.hero-content {
  color: var(--white);
  z-index: 2;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1rem;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  border-radius: 50px;
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 2rem;
  border: 1px solid rgba(255, 255, 255, 0.2);
  animation: fadeInUp 1s ease-out;
}

.hero-title {
  font-size: 4rem;
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  animation: fadeInUp 1s ease-out 0.2s both;
}

.hero-title .highlight {
  background: linear-gradient(135deg, var(--accent-color), #fbbf24);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-subtitle {
  font-size: 1.25rem;
  line-height: 1.6;
  margin-bottom: 3rem;
  opacity: 0.9;
  max-width: 500px;
  animation: fadeInUp 1s ease-out 0.4s both;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  margin-bottom: 3rem;
  animation: fadeInUp 1s ease-out 0.6s both;
}

.btn-primary,
.btn-secondary {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  border-radius: 12px;
  font-weight: 600;
  font-size: 1rem;
  text-decoration: none;
  transition: var(--transition);
  border: 2px solid transparent;
}

.btn-primary {
  background: var(--gradient-accent);
  color: var(--white);
  box-shadow: var(--shadow-lg);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-xl);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.15);
  color: var(--white);
  backdrop-filter: blur(10px);
  border-color: rgba(255, 255, 255, 0.3);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.25);
  transform: translateY(-3px);
}

.btn-primary.large,
.btn-secondary.large {
  padding: 1.25rem 2.5rem;
  font-size: 1.1rem;
}

.btn-outline {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  background: transparent;
  border: 2px solid var(--primary-color);
  color: var(--primary-color);
  border-radius: 12px;
  font-weight: 600;
  text-decoration: none;
  transition: var(--transition);
}

.btn-outline:hover {
  background: var(--primary-color);
  color: var(--white);
  transform: translateY(-2px);
}

.hero-stats {
  display: flex;
  gap: 2rem;
  animation: fadeInUp 1s ease-out 0.8s both;
}

.stat {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: 2rem;
  font-weight: 800;
  line-height: 1;
  margin-bottom: 0.25rem;
}

.stat-label {
  font-size: 0.875rem;
  opacity: 0.8;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

/* Hero Visual */
.hero-visual {
  position: relative;
  animation: fadeInRight 1s ease-out 0.4s both;
}

.hero-image-container {
  position: relative;
}

.image-backdrop {
  position: absolute;
  inset: -2rem;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 2rem;
  backdrop-filter: blur(20px);
  transform: rotate(-3deg);
}

.hero-image {
  width: 100%;
  height: 500px;
  object-fit: cover;
  border-radius: 2rem;
  box-shadow: var(--shadow-xl);
  position: relative;
  z-index: 2;
}

.floating-elements {
  position: absolute;
  inset: 0;
  z-index: 3;
}

.floating-card {
  position: absolute;
  background: var(--white);
  padding: 1rem 1.5rem;
  border-radius: 12px;
  box-shadow: var(--shadow-lg);
  display: flex;
  align-items: center;
  gap: 0.75rem;
  color: var(--text-dark);
  font-weight: 600;
  animation: float-card 6s ease-in-out infinite;
}

.floating-card:nth-child(1) {
  top: 10%;
  right: -10%;
  animation-delay: 0s;
}

.floating-card:nth-child(2) {
  bottom: 30%;
  left: -15%;
  animation-delay: 2s;
}

.floating-card:nth-child(3) {
  bottom: 10%;
  right: 10%;
  animation-delay: 4s;
}

.floating-card i {
  color: var(--accent-color);
  font-size: 1.25rem;
}

@keyframes float-card {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translateX(30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

/* Quick Access Section */
.quick-access {
  padding: 6rem 0;
  background: var(--bg-light);
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-header h2 {
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 1rem;
}

.section-header p {
  font-size: 1.125rem;
  color: var(--text-light);
  max-width: 600px;
  margin: 0 auto;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.access-card {
  background: var(--white);
  padding: 2rem;
  border-radius: 20px;
  text-decoration: none;
  color: var(--text-dark);
  box-shadow: var(--shadow);
  transition: var(--transition);
  display: flex;
  align-items: center;
  gap: 1.5rem;
  position: relative;
  overflow: hidden;
}

.access-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  background: var(--gradient-primary);
  transform: scaleY(0);
  transition: var(--transition);
}

.access-card.programs::before { background: var(--gradient-primary); }
.access-card.admissions::before { background: var(--gradient-accent); }
.access-card.campus::before { background: linear-gradient(135deg, var(--success-color), #059669); }
.access-card.news::before { background: linear-gradient(135deg, #8b5cf6, #7c3aed); }
.access-card.library::before { background: linear-gradient(135deg, #f59e0b, #d97706); }
.access-card.contact::before { background: linear-gradient(135deg, #10b981, #059669); }

.access-card:hover::before {
  transform: scaleY(1);
}

.access-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-xl);
}

.card-icon {
  width: 60px;
  height: 60px;
  border-radius: 16px;
  background: var(--gradient-primary);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.card-icon i {
  font-size: 1.5rem;
  color: var(--white);
}

.card-content {
  flex: 1;
}

.card-content h3 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: var(--text-dark);
}

.card-content p {
  color: var(--text-light);
  line-height: 1.5;
  margin-bottom: 1rem;
}

.card-badge {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  background: var(--bg-light);
  color: var(--primary-color);
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.card-arrow {
  color: var(--text-lighter);
  transition: var(--transition);
}

.access-card:hover .card-arrow {
  color: var(--primary-color);
  transform: translateX(4px);
}

/* Features Section */
.features-section {
  padding: 6rem 0;
}

.features-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.section-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1rem;
  background: var(--bg-light);
  color: var(--primary-color);
  border-radius: 50px;
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
}

.features-text h2 {
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.features-text p {
  font-size: 1.125rem;
  color: var(--text-light);
  line-height: 1.6;
  margin-bottom: 2rem;
}

.features-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.feature-check {
  width: 32px;
  height: 32px;
  border-radius: 8px;
  background: var(--success-color);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  margin-top: 0.25rem;
}

.feature-check i {
  color: var(--white);
  font-size: 0.875rem;
}

.feature-text h4 {
  font-size: 1.125rem;
  font-weight: 600;
  color: var(--text-dark);
  margin-bottom: 0.25rem;
}

.feature-text p {
  color: var(--text-light);
  font-size: 1rem;
  line-height: 1.5;
  margin: 0;
}

.visual-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 1rem;
  height: 500px;
}

.visual-item {
  border-radius: 16px;
  overflow: hidden;
  box-shadow: var(--shadow-lg);
  transition: var(--transition);
}

.visual-item.large {
  grid-row: 1 / -1;
}

.visual-item:hover {
  transform: scale(1.02);
  box-shadow: var(--shadow-xl);
}

.visual-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* CTA Section */
.cta-section {
  position: relative;
  padding: 6rem 0;
  color: var(--white);
  text-align: center;
  overflow: hidden;
}

.cta-background {
  position: absolute;
  inset: 0;
  background: var(--gradient-primary);
}

.cta-overlay {
  position: absolute;
  inset: 0;
  background: url('../assets/img/images/banner.jpg') center/cover;
  opacity: 0.2;
}

.cta-pattern {
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle at 30% 70%, rgba(255, 255, 255, 0.1) 2px, transparent 2px);
  background-size: 60px 60px;
}

.cta-content {
  position: relative;
  z-index: 2;
  max-width: 800px;
  margin: 0 auto;
}

.cta-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1rem;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  border-radius: 50px;
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 2rem;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.cta-content h2 {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.cta-content p {
  font-size: 1.25rem;
  line-height: 1.6;
  margin-bottom: 3rem;
  opacity: 0.9;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-bottom: 2rem;
  flex-wrap: wrap;
}

.cta-note {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  font-size: 0.875rem;
  opacity: 0.8;
}

/* News Preview */
.news-preview {
  padding: 6rem 0;
  background: var(--bg-light);
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 3rem;
}

.view-all-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--primary-color);
  text-decoration: none;
  font-weight: 600;
  transition: var(--transition);
}

.view-all-link:hover {
  gap: 0.75rem;
}

.news-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.news-card {
  background: var(--white);
  border-radius: 16px;
  overflow: hidden;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

.news-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-xl);
}

.news-image {
  position: relative;
  height: 200px;
  overflow: hidden;
}

.news-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: var(--transition);
}

.news-card:hover .news-image img {
  transform: scale(1.05);
}

.news-category {
  position: absolute;
  top: 1rem;
  left: 1rem;
  padding: 0.25rem 0.75rem;
  background: var(--accent-color);
  color: var(--white);
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.news-content {
  padding: 1.5rem;
}

.news-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  font-size: 0.875rem;
  color: var(--text-light);
}

.news-content h3 {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-dark);
  margin-bottom: 0.75rem;
  line-height: 1.4;
}

.news-content p {
  color: var(--text-light);
  line-height: 1.6;
  margin-bottom: 1rem;
}

.read-more {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--primary-color);
  text-decoration: none;
  font-weight: 600;
  font-size: 0.875rem;
  transition: var(--transition);
}

.read-more:hover {
  gap: 0.75rem;
}

/* Responsive Design */
@media (max-width: 1024px) {
  .hero-container {
    grid-template-columns: 1fr;
    gap: 2rem;
    text-align: center;
  }
  
  .hero-title {
    font-size: 3rem;
  }
  
  .features-content {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  
  .section-header {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }
}

@media (max-width: 768px) {
  .hero-container {
    padding: 0 1rem;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-buttons {
    flex-direction: column;
    align-items: center;
  }
  
  .hero-stats {
    justify-content: center;
  }
  
  .cards-grid {
    grid-template-columns: 1fr;
  }
  
  .access-card {
    flex-direction: column;
    text-align: center;
  }
  
  .cta-content h2 {
    font-size: 2rem;
  }
  
  .cta-buttons {
    flex-direction: column;
    align-items: center;
  }
  
  .floating-card {
    display: none;
  }
}

@media (max-width: 480px) {
  .hero-title {
    font-size: 2rem;
  }
  
  .section-header h2 {
    font-size: 2rem;
  }
  
  .features-text h2 {
    font-size: 2rem;
  }
  
  .visual-grid {
    grid-template-columns: 1fr;
    height: auto;
  }
  
  .visual-item.large {
    grid-row: auto;
  }
  
  .news-grid {
    grid-template-columns: 1fr;
  }
}
</style> 