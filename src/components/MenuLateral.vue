<template>
  <div>
    <div class="sidebar" :class="{ open: isOpen }">
      <button @click="toggleMenu" class="menu-button">
        <i v-if="!isOpen" class="fas fa-bars">+</i>
        <i v-else class="fas fa-times">-</i>
      </button>
      <nav class="menu">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>

<style lang="scss">
$menu-width: 200px;
$menu-width-hidden: 10px;

.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  width: $menu-width-hidden;
  background-color: #f5f5f5;
  box-shadow: 2px 0px 3px rgba(0, 0, 0, 0.1);
  padding: 20px;
  transition: all 0.2s ease;

  .menu-button {
    position: absolute;
    top: 15px;
    right: 15px;
    border: none;
    background-color: transparent;
    outline: none;
    cursor: pointer;

    i {
      font-size: 24px;
    }
  }

  .menu {
    display: none;
    margin-top: 50px;

    a {
      display: block;
      padding: 10px;
      text-decoration: none;
      color: #333;
      transition: background-color 0.2s ease;

      &:hover {
        background-color: #e5e5e5;
      }
    }
  }

  &.open {
    width: $menu-width;
    .menu {
      display: block;
    }
  }
}
</style>
