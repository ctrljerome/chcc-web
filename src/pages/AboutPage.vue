<template>
  <div class="about-page">
    <!-- Hero / Banner -->
    <section class="about-hero">
      <div class="hero-background">
        <div class="hero-overlay"></div>
        <div class="hero-pattern"></div>
      </div>
      <div class="hero-content">
        <div class="hero-badge">
          <span>Est. 1990</span>
        </div>
        <h1>About CHCC</h1>
        <p>Discover our legacy of excellence in education, service, and community. Learn about our mission, values, and commitment to shaping future leaders through faith-inspired learning.</p>
        <div class="hero-stats">
          <div class="stat">
            <span class="stat-number">30+</span>
            <span class="stat-label">Years of Excellence</span>
          </div>
          <div class="stat">
            <span class="stat-number">5000+</span>
            <span class="stat-label">Alumni</span>
          </div>
          <div class="stat">
            <span class="stat-number">50+</span>
            <span class="stat-label">Faculty Members</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Mission, Vision, Values -->
    <section class="mission-vision-values">
      <div class="container">
        <div class="section-header">
          <h2>Our Foundation</h2>
          <p>The principles that guide everything we do</p>
        </div>
        
        <div class="mvv-grid">
          <div class="mvv-item mission">
            <div class="mvv-icon">
              <i class="pi pi-compass"></i>
            </div>
            <h3>Our Mission</h3>
            <p>To become a God-centered learning institution focused on holistic education that forms and educates individuals to become conscientious, compassionate, competent, and committed persons towards the development of a just and humane society.</p>
          </div>
          
          <div class="mvv-item vision">
            <div class="mvv-icon">
              <i class="pi pi-eye"></i>
            </div>
            <h3>Our Vision</h3>
            <p>Concepcion Holy Cross College is an institution for academic and values formation offering relevant, learner-centered, and values-oriented programs that produce competent persons of character in the service of God and society.</p>
          </div>
          

          <div class="mvv-item vision">
            <div class="mvv-icon">
              <i class="pi pi-eye"></i>
            </div>
            <h3>Our Goals</h3>
            <p>The Concepcion Holy Cross College, Inc. is committed to achieve the following goals and objectives in pursuit of its mission:
              <br> • To develop a Christ-centered community <br> • To produce intellectually-competent and wholly-developed graduates <br>• To emphasize self-realization without compromising human dignity and moral values</p>
          </div>

        </div>
      </div>
    </section>

    <!-- History Timeline -->
    <section class="history-section">
      <div class="container">
        <div class="section-header">
          <h2>Our Journey</h2>
          <p>Milestones that shaped our institution</p>
        </div>
        
        <div class="timeline">
          <div class="timeline-line"></div>
          <div 
            class="timeline-item" 
            v-for="(event, index) in historyEvents" 
            :key="index"
            :class="{ 'timeline-item-right': index % 2 === 1 }"
          >
            <div class="timeline-marker">
              <div class="timeline-dot"></div>
              <div class="timeline-year">{{ event.year }}</div>
            </div>
            <div class="timeline-content">
              <div class="timeline-card">
                <h3>{{ event.title }}</h3>
                <p>{{ event.description }}</p>
                <div class="timeline-badge">{{ event.category }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Why Choose Us -->
    <section class="why-us">
      <div class="container">
        <div class="section-header">
          <h2>Why Choose CHCC?</h2>
          <p>Discover what makes us different and why students thrive here</p>
        </div>
        
        <div class="features-grid">
          <div class="feature-card" v-for="(feature, index) in features" :key="index">
            <div class="feature-icon">
              <i :class="feature.icon"></i>
            </div>
            <div class="feature-content">
              <h3>{{ feature.title }}</h3>
              <p>{{ feature.text }}</p>
              <div class="feature-highlight">{{ feature.highlight }}</div>
            </div>
            <div class="feature-arrow">
              <i class="pi pi-arrow-right"></i>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Leadership Section -->
    <section class="leadership-section">
      <div class="container">
        <div class="section-header">
          <h2>Board of Trustees</h2>
          <p>Meet the dedicated individuals guiding our institution</p>
        </div>
        
        <div class="leadership-grid">
          <div class="leader-card" v-for="(leader, index) in leadership" :key="index">
            <div class="leader-image">
              <img :src="leader.image" :alt="leader.name" />
            </div>
            <div class="leader-info">
              <h4>{{ leader.name }}</h4>
              <p class="leader-title">{{ leader.position }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const historyEvents = ref([
  { 
    year: '1990', 
    title: 'Foundation', 
    description: 'Concepcion Holy Cross College was established with a vision to provide quality Christian education to the community.',
    category: 'Establishment'
  },
  { 
    year: '1995', 
    title: 'First Programs', 
    description: 'Launched initial academic programs in Education, Business Administration, and Liberal Arts.',
    category: 'Academic Growth'
  },
  { 
    year: '2000', 
    title: 'First Graduation', 
    description: 'Celebrated our inaugural graduation ceremony with 120 proud graduates who continue to serve their communities.',
    category: 'Milestone'
  },
  { 
    year: '2005', 
    title: 'Accreditation', 
    description: 'Received full accreditation from CHED, validating our commitment to educational excellence.',
    category: 'Recognition'
  },
  { 
    year: '2010', 
    title: 'Campus Expansion', 
    description: 'Opened new state-of-the-art facilities including modern library, computer labs, and sports complex.',
    category: 'Infrastructure'
  },
  { 
    year: '2015', 
    title: 'Digital Integration', 
    description: 'Implemented comprehensive digital learning platforms and smart classroom technologies.',
    category: 'Innovation'
  },
  { 
    year: '2020', 
    title: 'Pandemic Resilience', 
    description: 'Successfully transitioned to hybrid learning model, ensuring continuity of education during challenging times.',
    category: 'Adaptation'
  },
  { 
    year: '2024', 
    title: 'Future Vision', 
    description: 'Launched strategic plan for sustainable growth and enhanced community partnerships.',
    category: 'Future'
  }
])

const features = ref([
  { 
    icon: 'pi pi-graduation-cap', 
    title: 'Academic Excellence', 
    text: 'Comprehensive curriculum designed to meet industry standards and prepare students for successful careers.',
    highlight: '95% Graduate Employment Rate'
  },
  { 
    icon: 'pi pi-users', 
    title: 'Expert Faculty', 
    text: 'Dedicated professors with advanced degrees and extensive industry experience committed to student success.',
    highlight: '15:1 Student-Faculty Ratio'
  },
  { 
    icon: 'pi pi-globe', 
    title: 'Global Perspective', 
    text: 'International partnerships and exchange programs that broaden horizons and create global opportunities.',
    highlight: '10+ Partner Universities'
  },
  { 
    icon: 'pi pi-home', 
    title: 'Campus Life', 
    text: 'Vibrant campus community with modern facilities, student organizations, and enriching extracurricular activities.',
    highlight: '50+ Student Organizations'
  },
  { 
    icon: 'pi pi-lightbulb', 
    title: 'Innovation Hub', 
    text: 'State-of-the-art laboratories, research facilities, and technology centers fostering creativity and innovation.',
    highlight: 'Latest Technology Integration'
  },
  { 
    icon: 'pi pi-heart', 
    title: 'Faith & Service', 
    text: 'Strong emphasis on Christian values, community service, and developing compassionate leaders.',
    highlight: '1000+ Community Service Hours'
  }
])

const leadership = ref([
  {
    name: 'RAQUEL T. STA INES, Ph.D.',
    position: 'Chairperson',
    image: '../assets/img/team/president.jpg'
  },
  {
    name: 'DAVID P. STA INES, JR.',
    position: 'Vice-chairperson',
    image: '../assets/img/team/vp-academic.jpg'
  },
  {
    name: 'DANA GENEROSA SI. MARCELO',
    position: 'Member',
    image: '../assets/img/team/dean.jpg'
  },
  {
    name: 'DOLORES RAQUEL S. SALVADOR, MD, MHPEd',
    position: 'Member',
    image: '../assets/img/team/dean.jpg'
  },
  {
    name: 'DANIEL PABLO T. STA INES, MS-IDT, RRT-NPS',
    position: 'Member',
    image: '../assets/img/team/dean.jpg'
  }
])
</script>

<style scoped>
:root {
  --primary-color: #1e40af;
  --primary-light: #3b82f6;
  --primary-dark: #1e3a8a;
  --accent-color: #f59e0b;
  --accent-hover: #d97706;
  --text-dark: #1f2937;
  --text-light: #6b7280;
  --text-lighter: #9ca3af;
  --border-color: #e5e7eb;
  --bg-light: #f8fafc;
  --bg-lighter: #f1f5f9;
  --white: #ffffff;
  --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --gradient-primary: linear-gradient(135deg, var(--primary-color), var(--primary-light));
  --gradient-accent: linear-gradient(135deg, var(--accent-color), var(--accent-hover));
}

.about-page {
  overflow-x: hidden;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

/* Hero Section */
.about-hero {
  position: relative;
  min-height: 600px;
  display: flex;
  align-items: center;
  color: var(--white);
  overflow: hidden;
}

.hero-background {
  position: absolute;
  inset: 0;
  background: var(--gradient-primary);
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: url('../assets/img/images/banner.jpg') center/cover;
  opacity: 0.7;
}

.hero-pattern {
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle at 25% 25%, rgba(255, 255, 255, 0.1) 2px, transparent 2px);
  background-size: 40px 40px;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  text-align: center;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  padding: 0.5rem 1rem;
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(10px);
  border-radius: 50px;
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 2rem;
  border: 1px solid rgba(255, 255, 255, 0.3);
}

.hero-content h1 {
  font-size: 3.5rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  background: linear-gradient(to right, var(--white), rgba(255, 255, 255, 0.8));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-content p {
  font-size: 1.25rem;
  line-height: 1.6;
  margin-bottom: 3rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  opacity: 0.9;
}

.hero-stats {
  display: flex;
  justify-content: center;
  gap: 3rem;
  flex-wrap: wrap;
}

.stat {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: 2.5rem;
  font-weight: 800;
  line-height: 1;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 0.875rem;
  opacity: 0.8;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

/* Section Headers */
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

/* Mission Vision Values */
.mission-vision-values {
  padding: 3rem 0;
  background: var(--bg-light);
}

.mvv-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.mvv-item {
  background: var(--white);
  padding: 2rem;
  border-radius: 20px;
  box-shadow: var(--shadow);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.mvv-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--gradient-primary);
}

.mvv-item.mission::before { background: var(--gradient-primary); }
.mvv-item.vision::before { background: var(--gradient-accent); }
.mvv-item.values::before { background: linear-gradient(135deg, #10b981, #059669); }

.mvv-item:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.mvv-icon {
  width: 60px;
  height: 60px;
  border-radius: 15px;
  background: var(--gradient-primary);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.mvv-icon i {
  font-size: 1.5rem;
  color: var(--white);
}

.mvv-item h3 {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--text-dark);
  margin-bottom: 1rem;
}

.mvv-item p {
  color: var(--text-light);
  line-height: 1.7;
}

.values-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}

.value-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem;
  background: var(--bg-light);
  border-radius: 10px;
  transition: var(--transition);
}

.value-item:hover {
  background: var(--primary-color);
  color: var(--white);
  transform: scale(1.05);
}

.value-item i {
  color: var(--accent-color);
  font-size: 0.875rem;
}

.value-item:hover i {
  color: var(--white);
}

/* Timeline */
.history-section {
  padding: 6rem 0;
}

.timeline {
  position: relative;
  max-width: 800px;
  margin: 0 auto;
}

.timeline-line {
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 2px;
  background: var(--gradient-primary);
  transform: translateX(-50%);
}

.timeline-item {
  display: flex;
  margin-bottom: 3rem;
  align-items: center;
}

.timeline-item-right {
  flex-direction: row-reverse;
}

.timeline-marker {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 2rem;
  z-index: 2;
}

.timeline-dot {
  width: 16px;
  height: 16px;
  background: var(--white);
  border: 4px solid var(--primary-color);
  border-radius: 50%;
  margin-bottom: 0.5rem;
}

.timeline-year {
  background: var(--primary-color);
  color: var(--white);
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: 600;
  white-space: nowrap;
}

.timeline-content {
  flex: 1;
  max-width: 350px;
}

.timeline-card {
  background: var(--white);
  padding: 1.5rem;
  border-radius: 15px;
  box-shadow: var(--shadow);
  transition: var(--transition);
  position: relative;
}

.timeline-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
}

.timeline-card h3 {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-dark);
  margin-bottom: 0.75rem;
}

.timeline-card p {
  color: var(--text-light);
  line-height: 1.6;
  margin-bottom: 1rem;
}

.timeline-badge {
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

/* Features */
.why-us {
  padding: 6rem 0;
  background: var(--bg-light);
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.feature-card {
  background: var(--white);
  padding: 2rem;
  border-radius: 20px;
  box-shadow: var(--shadow);
  transition: var(--transition);
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  position: relative;
  overflow: hidden;
}

.feature-card::before {
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

.feature-card:hover::before {
  transform: scaleY(1);
}

.feature-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.feature-icon {
  width: 60px;
  height: 60px;
  border-radius: 15px;
  background: var(--gradient-accent);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.feature-icon i {
  font-size: 1.5rem;
  color: var(--white);
}

.feature-content {
  flex: 1;
}

.feature-content h3 {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-dark);
  margin-bottom: 0.75rem;
}

.feature-content p {
  color: var(--text-light);
  line-height: 1.6;
  margin-bottom: 1rem;
}

.feature-highlight {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  background: var(--gradient-accent);
  color: var(--white);
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 600;
}

.feature-arrow {
  color: var(--text-lighter);
  transition: var(--transition);
}

.feature-card:hover .feature-arrow {
  color: var(--primary-color);
  transform: translateX(4px);
}

/* Leadership */
.leadership-section {
  padding: 6rem 0;
}

.leadership-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.leader-card {
  background: var(--white);
  border-radius: 20px;
  overflow: hidden;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

.leader-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.leader-image {
  height: 250px;
  overflow: hidden;
  background: var(--bg-light);
}

.leader-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: var(--transition);
}

.leader-card:hover .leader-image img {
  transform: scale(1.05);
}

.leader-info {
  padding: 1.5rem;
}

.leader-info h4 {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--text-dark);
  margin-bottom: 0.5rem;
}

.leader-title {
  color: var(--primary-color);
  font-weight: 600;
  margin-bottom: 1rem;
}

.leader-description {
  color: var(--text-light);
  line-height: 1.6;
}

/* Responsive Design */
@media (max-width: 768px) {
  .hero-content h1 {
    font-size: 2.5rem;
  }
  
  .hero-stats {
    gap: 1.5rem;
  }
  
  .section-header h2 {
    font-size: 2rem;
  }
  
  .mvv-grid {
    grid-template-columns: 1fr;
  }
  
  .timeline-line {
    left: 2rem;
  }
  
  .timeline-item,
  .timeline-item-right {
    flex-direction: row;
    padding-left: 4rem;
  }
  
  .timeline-marker {
    position: absolute;
    left: -1rem;
    margin: 0;
  }
  
  .features-grid {
    grid-template-columns: 1fr;
  }
  
  .feature-card {
    flex-direction: column;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .hero-content {
    padding: 0 1rem;
  }
  
  .hero-content h1 {
    font-size: 2rem;
  }
  
  .hero-stats {
    flex-direction: column;
    gap: 1rem;
  }
  
  .container {
    padding: 0 0.5rem;
  }
  
  .mvv-item,
  .timeline-card,
  .feature-card {
    padding: 1.5rem;
  }
}
</style>