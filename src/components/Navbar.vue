<template>
  <nav class="navbar">
    <!-- Logo Section -->
    <div class="navbar-brand">
      <img src="../assets/img/logos/mainlogo.png" alt="CHCC Logo" class="logo-img" />
      <span class="brand-text">Concepcion Holy <br>Cross College Inc.</span>
    </div>



    <!-- Desktop Navigation -->
    <div class="navbar-nav">
      <router-link 
        v-for="item in items" 
        :key="item.label"
        :to="item.to" 
        class="nav-link"
      >
        {{ item.label }}
      </router-link>
    </div>

    <!-- Action Buttons -->
    <div class="navbar-actions">
      <button class="btn-portal">
        <i class="pi pi-user"></i>
        Student Portal
      </button>
      <button class="btn-apply">
        <i class="pi pi-plus"></i>
        Apply Now
      </button>
    </div>

    <!-- Mobile Menu Button -->
    <button class="mobile-toggle" @click="toggleMobile">
      <i class="pi pi-bars"></i>
    </button>

    <!-- Mobile Menu -->
    <div class="mobile-menu" :class="{ active: mobileOpen }">
      <router-link 
        v-for="item in items" 
        :key="item.label"
        :to="item.to" 
        class="mobile-link"
        @click="mobileOpen = false"
      >
        {{ item.label }}
      </router-link>
      <div class="mobile-actions">
        <button class="btn-portal">Student Portal</button>
        <button class="btn-apply">Apply Now</button>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const mobileOpen = ref(false)

const items = ref([
  { label: 'Home', to: '/' },
  { label: 'About', to: '/about' },
  { label: 'Admissions', to: '/admissions' },
  { label: 'Programs', to: '/programs' },
  { label: 'Courses', to: '/courses' },
  { label: 'Faculty', to: '/faculty' },
  { label: 'News', to: '/news' },
  { label: 'Contact', to: '/contact' }
])

const toggleMobile = () => {
  mobileOpen.value = !mobileOpen.value
}
</script>

<style>
/* Global reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  background: #ffffff;
  border-bottom: 1px solid #e5e7eb;
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 2rem;
  height: 64px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

/* Brand */
.navbar-brand {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}
.logo-img {
  height: 40px;   /* adjust depending on your navbar height */
  width: auto;
  object-fit: contain;
}


.logo {
  width: 36px;
  height: 36px;
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 1.1rem;
}

.brand-text {
  font-size: 1.25rem;
  font-weight: 700;
  color: #1e40af;
}

/* Navigation */
.navbar-nav {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.nav-link {
  padding: 0.5rem 1rem;
  color: #374151;
  text-decoration: none;
  border-radius: 6px;
  font-weight: 500;
  font-size: 0.9rem;
  transition: all 0.2s ease;
}

.nav-link:hover {
  background: #f3f4f6;
  color: #1e40af;
}

.nav-link.router-link-active {
  background: #dbeafe;
  color: #1e40af;
}

/* Actions */
.navbar-actions {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.btn-portal,
.btn-apply {
  padding: 0.5rem 1rem;
  border-radius: 6px;
  font-weight: 500;
  font-size: 0.875rem;
  cursor: pointer;
  border: none;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  transition: all 0.2s ease;
}

.btn-portal {
  background: white;
  color: #374151;
  border: 1px solid #d1d5db;
}

.btn-portal:hover {
  background: #f9fafb;
  border-color: #9ca3af;
}

.btn-apply {
  background: #f59e0b;
  color: white;
}

.btn-apply:hover {
  background: #d97706;
}

/* Mobile */
.mobile-toggle {
  display: none;
  background: none;
  border: none;
  font-size: 1.5rem;
  color: #374151;
  cursor: pointer;
  padding: 0.25rem;
}

.mobile-menu {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  background: white;
  border-bottom: 1px solid #e5e7eb;
  padding: 1rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.mobile-menu.active {
  display: block;
}

.mobile-link {
  display: block;
  padding: 0.75rem;
  color: #374151;
  text-decoration: none;
  border-bottom: 1px solid #f3f4f6;
}

.mobile-link:hover {
  background: #f9fafb;
}

.mobile-actions {
  padding-top: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.mobile-actions .btn-portal,
.mobile-actions .btn-apply {
  width: 100%;
  justify-content: center;
}

/* Responsive */
@media (max-width: 1024px) {
  .navbar {
    padding: 0 1.5rem;
  }
  
  .navbar-nav {
    gap: 0.25rem;
  }
  
  .nav-link {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
}

@media (max-width: 768px) {
  .navbar {
    padding: 0 1rem;
  }
  
  .navbar-nav,
  .navbar-actions {
    display: none;
  }
  
  .mobile-toggle {
    display: block;
  }
}

/* Body padding to account for fixed navbar */
body {
  padding-top: 64px;
  margin: 0;
  background: white;
}
</style>