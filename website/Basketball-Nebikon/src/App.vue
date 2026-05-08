<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav class="navbar">
      <div class="logo">NEBI<span>KON</span></div>

      <div class="nav-links">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/schedule">Training & Spiele</RouterLink>
        <RouterLink to="/teams">Teams</RouterLink>
        <RouterLink to="/join" class="btn-join">Mitmachen</RouterLink>
      </div>
    </nav>
  </header>

  <!-- Hier werden die Seiten (Views) geladen -->
  <main>
    <RouterView />
  </main>

  <footer class="footer">
    <p>&copy; 2026 Basketball Nebikon. Built for the Game.</p>
  </footer>
</template>

<style>
/* GLOBALE STYLES (Aus eurem Styleguide) */
:root {
  --orange: #F58220;
  --cyan: #00AEEF;
  --navy: #0B1B32;
  --bg: #0B111B;
  --white: #FFFFFF;
}

body {
  background-color: var(--bg);
  color: var(--white);
  font-family: 'Inter', sans-serif;
  margin: 0;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 5%;
  background: rgba(11, 17, 27, 0.9);
  backdrop-filter: blur(10px);
  position: sticky;
  top: 0;
  z-index: 100;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}

.logo {
  font-family: 'Outfit', sans-serif;
  font-weight: 900;
  font-size: 1.5rem;
  text-transform: uppercase;
}
.logo span { color: var(--orange); }

.nav-links {
  display: flex;
  gap: 25px;
  align-items: center;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.9rem;
  transition: 0.3s;
}

.nav-links a:hover { color: var(--cyan); }

/* Aktiver Link Style */
.router-link-active:not(.btn-join) {
  color: var(--orange) !important;
}

.btn-join {
  background: var(--orange);
  padding: 10px 20px;
  border-radius: 8px;
  color: white !important;
}

.btn-join:hover {
  transform: scale(1.05);
  box-shadow: 0 0 20px rgba(245, 130, 32, 0.4);
}

.footer {
  padding: 40px;
  text-align: center;
  opacity: 0.5;
  font-size: 0.8rem;
}
</style>
