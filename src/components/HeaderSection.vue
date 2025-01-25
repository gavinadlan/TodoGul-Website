<template>
  <header>
    <div class="logo">
      <a href="#hero">
        <h1>TODOGUL</h1>
      </a>
    </div>
    <nav :class="{ open: isMenuOpen }">
      <a href="#about" @click="toggleMenu">About</a>
      <a href="#features" @click="toggleMenu">Features</a>
      <a href="#reviews" @click="toggleMenu">Reviews</a>
      <a href="#contact" @click="toggleMenu">Contact</a>
    </nav>
    <button class="menu-toggle" @click="toggleMenu" aria-label="Toggle menu">
      <i :class="isMenuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
    </button>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false, // State untuk menyimpan status menu (buka/tutup)
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen; // Ubah status menu
    },
  },
};
</script>

<style scoped>
/* Header Style */
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px;
  background-color: #8875ff;
  color: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
}

/* Logo */
.logo a {
  text-decoration: none;
}

.logo h1 {
  margin: 0;
  font-size: 1.75rem;
  font-weight: bold;
  letter-spacing: 2px;
  color: white;
}

/* Navigation */
nav {
  display: flex;
  gap: 20px;
  transition: transform 0.3s ease-in-out;
}

/* Link Style */
nav a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  font-weight: 500;
  transition: color 0.3s ease;
}

nav a:hover {
  color: #f8f9ff;
}

/* Menu Toggle (hidden by default on desktop) */
.menu-toggle {
  display: none;
  background: none;
  border: none;
  color: white;
  font-size: 1.5rem;
  cursor: pointer;
}

/* Responsive Styling */
@media (max-width: 768px) {
  nav {
    position: fixed;
    top: 0;
    right: 0;
    height: 100%;
    width: 250px;
    background-color: #8875ff;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 30px;
    transform: translateX(100%); /* Hide off-screen */
  }

  nav.open {
    transform: translateX(0); /* Show menu */
  }

  nav a {
    font-size: 1.25rem;
  }

  .menu-toggle {
    display: block;
  }
}
</style>
