<template>
  <nav class="navbar">
    <div class="navbar-brand">
      <button
        class="navbar-burger"
        @click="toggleMenu"
        :class="{ 'is-active': isMenuActive }"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>

    <div class="navbar-menu" :class="{ 'is-active': isMenuActive }">
      <div class="navbar-start">
        <ul>
          <li>
            <a href="#home">Home</a>
          </li>
          <li>
            <a href="#about">About</a>
          </li>
          <li>
            <a href="#Edu">Education</a>
          </li>
          <li>
            <a href="#project">Projects</a>
          </li>
          <li>
            <a href="#contacts">Contacts</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'NavbarComp',
  setup() {
    const isMenuActive = ref(false);

    const toggleMenu = () => {
      isMenuActive.value = !isMenuActive.value;
    };

    return {
      isMenuActive,
      toggleMenu,
    };
  },
};
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}

.navbar {
  background-color: #ccd8c1;
  text-align: center; /* Center text */
  padding: 30px;
  position: fixed;
  top: 10px;
  width: 95%; /* Ensure full width */
  z-index: 1000;
}

.navbar-start {
  display: flex;
  justify-content: center; /* Center links */
  width: 100%;
}

.navbar-start ul {
  list-style: none;
  display: flex;
  gap: 15px;
  padding: 0;
  margin: 0;
}

.navbar-start li {
  display: inline-block;
}

.navbar-start a {
  text-decoration: none;
  color: #000000;
  padding: 10px;
  transition: color 0.3s ease-in-out;
}

.navbar-start a:hover {
  color: #2471be;
}


.navbar-item {
  color: #f1f1f1;
  padding: 10px;
}

.navbar-burger {
  background: transparent;
  border: none;
  cursor: pointer;
  display: none; /* Initially hide the burger */
}

.navbar-burger span {
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px auto;
  background: rgb(0, 0, 0);
}

.navbar-menu {
  display: flex;
  flex-direction: row;
}

.navbar-menu.is-active {
  display: flex;
  flex-direction: column;
}

@media (max-width: 500px) {
  .navbar {
    width: 80%;
  }

  .navbar-start ul {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .navbar-start li {
    width: 100%;
    text-align: center;
  }

  .navbar-start a {
    width: 100%;
  }

  /* Display the hamburger menu on small screens */
  .navbar-burger {
    display: block;
  }

  /* Adjust navbar links to be stacked in mobile view */
  .navbar-start {
    display: flex;
    flex-direction: column;
  }

  .navbar-item {
    margin-bottom: 10px;
  }

  .navbar-menu {
    display: none; /* Hide the menu by default */
  }

  .navbar-menu.is-active {
    display: flex;
  }
}
</style>
