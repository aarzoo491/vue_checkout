<template>
  <header class="navbar">
    <div class="navbar-container">
      <router-link to="/" class="logo">
        <span class="logo-icon">⚡</span>
        <span class="logo-text">AI Company</span>
      </router-link>

      <button class="menu-toggle" @click="isMenuOpen = !isMenuOpen">
        <span></span>
        <span></span>
        <span></span>
      </button>

      <nav class="nav-links" :class="{ active: isMenuOpen }">
        <router-link 
          to="/" 
          :class="{ active: isActive('/') }"
          @click="isMenuOpen = false"
        >
          Home
        </router-link>
        <router-link 
          to="/about" 
          :class="{ active: isActive('/about') }"
          @click="isMenuOpen = false"
        >
          About
        </router-link>
        <router-link 
          to="/services" 
          :class="{ active: isActive('/services') }"
          @click="isMenuOpen = false"
        >
          Services
        </router-link>
        <router-link 
          to="/checkout" 
          :class="{ active: isActive('/checkout') }"
          class="checkout-btn"
          @click="isMenuOpen = false"
        >
          Checkout
        </router-link>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
import { useRoute } from 'vue-router';
import { ref } from 'vue';

const route = useRoute();
const isMenuOpen = ref(false);

const isActive = (path: string) => {
  return route.path === path;
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* NAVBAR BASE */
.navbar {
  position: sticky;
  top: 0;
  width: 100%;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.95) 0%, rgba(245, 248, 255, 0.95) 100%);
  backdrop-filter: blur(15px);
  border-bottom: 1px solid rgba(102, 126, 234, 0.1);
  z-index: 999;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}

.navbar-container {
  width: 100%;
  padding: 0 5%;
  max-width: 1400px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
}

/* LOGO */
.logo {
  display: flex;
  align-items: center;
  gap: 8px;
  text-decoration: none;
  transition: all 0.3s ease;
  cursor: pointer;
  padding: 5px 10px;
  border-radius: 8px;
}

.logo:hover {
  background-color: rgba(102, 126, 234, 0.1);
}

.logo-icon {
  font-size: 28px;
  display: inline-block;
}

.logo-text {
  font-size: 20px;
  font-weight: 700;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  white-space: nowrap;
}

/* NAV LINKS */
.nav-links {
  display: flex;
  gap: 40px;
  align-items: center;
}

.nav-links a {
  text-decoration: none;
  font-size: 15px;
  font-weight: 500;
  color: #333;
  position: relative;
  padding: 8px 4px;
  transition: all 0.3s ease;
  white-space: nowrap;
  border-radius: 4px;
}

/* Animated underline */
.nav-links a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0%;
  height: 2px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  transition: width 0.3s ease;
}

.nav-links a:hover::after,
.nav-links a.active::after {
  width: 100%;
}

.nav-links a:hover {
  color: #667eea;
}

.nav-links a.active {
  color: #667eea;
  font-weight: 600;
}

/* Checkout Button */
.nav-links a.checkout-btn {
  padding: 10px 24px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white !important;
  border-radius: 6px;
  border: none;
  font-weight: 600;
  margin-left: 10px;
  cursor: pointer;
}

.nav-links a.checkout-btn::after {
  display: none;
}

.nav-links a.checkout-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
  color: white !important;
}

/* MENU TOGGLE (Hamburger) */
.menu-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 5px;
}

.menu-toggle span {
  width: 25px;
  height: 3px;
  background-color: #333;
  border-radius: 2px;
  transition: all 0.3s ease;
}

.menu-toggle:hover span {
  background-color: #667eea;
}

/* TABLET & MOBILE RESPONSIVE */
@media (max-width: 1024px) {
  .navbar-container {
    padding: 0 4%;
  }

  .nav-links {
    gap: 30px;
  }

  .nav-links a {
    font-size: 14px;
  }
}

@media (max-width: 768px) {
  .navbar-container {
    padding: 0 4%;
    height: 60px;
  }

  .logo-text {
    font-size: 18px;
  }

  .menu-toggle {
    display: flex;
  }

  .nav-links {
    position: absolute;
    top: 60px;
    left: 0;
    right: 0;
    width: 100%;
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(15px);
    border-bottom: 1px solid rgba(102, 126, 234, 0.1);
    flex-direction: column;
    gap: 0;
    padding: 20px 0;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
  }

  .nav-links.active {
    max-height: 400px;
  }

  .nav-links a {
    padding: 15px 5%;
    border-bottom: 1px solid rgba(0, 0, 0, 0.05);
    font-size: 15px;
    width: 100%;
  }

  .nav-links a.checkout-btn {
    margin-left: 5%;
    margin-right: 5%;
    margin-top: 10px;
  }

  .nav-links a:last-child {
    border-bottom: none;
  }
}

@media (max-width: 480px) {
  .navbar-container {
    padding: 0 3%;
    height: 55px;
  }

  .logo-icon {
    font-size: 24px;
  }

  .logo-text {
    font-size: 16px;
  }

  .nav-links a {
    font-size: 14px;
    padding: 12px 5%;
  }

  .nav-links a.checkout-btn {
    padding: 10px 5%;
    margin-left: 5%;
    margin-right: 5%;
  }
}
</style>
