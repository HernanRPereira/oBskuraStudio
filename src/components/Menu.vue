<template>
  <div class="dropdown">
    <button v-if="!isOpen" :class="{ 'dropbtn': true, 'closebtn': isOpen }" @click="toggleMenu">
      💀 MENÚ
    </button>
    <div v-if="isOpen" class="dropdown-content">
      <button class="menu-close-btn" @click="toggleMenu">
        ☠️ CLOSE
      </button>
      <a href="#" @click="closeMenu">About Us</a>
      <a href="#" @click="closeMenu">Gallery</a>
      <a href="#" @click="closeMenu">Contact Us</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    closeMenu() {
      this.isOpen = false;
    }
  }
};
</script>

<style scoped>
.dropdown {
  position: relative;
}

.dropbtn {
  background-color: transparent;
  color: black;
  border: none;
  padding: 1em;
  font-size: 1em;
  cursor: pointer;
  position: absolute;
  top: 1em;
  left: 1em;
  z-index: 1;
}

.closebtn {
  color: white;
}

.dropdown-content {
  position: fixed;
  top: 0;
  left: 0;
  width: 25%;
  height: 100%;
  background-color: black;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding-left: 5vh;
  justify-content: center;
  z-index: 0;
}

.menu-close-btn {
  background-color: transparent;
  color: white;
  border: none;
  padding: 1em;
  font-size: 1em;
  cursor: pointer;
  position: absolute;
  top: 3.5em;
  left: 3.5em;
}

.dropdown-content a {
  color: white;
  text-decoration: none;
  font-size: 5vh;
  padding: 1rem;
  text-align: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.dropdown-content a:hover {
  color: rgb(109, 132, 141);
}
</style>
