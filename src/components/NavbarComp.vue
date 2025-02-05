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
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
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
.navbar {
  background-color: #ccd8c1;
  text-align: right;
  padding: 30px;
  position: fixed;
  top: 10px;
  width: 95%;
  z-index: 1000;
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
