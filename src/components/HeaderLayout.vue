<template>
  <header class="header">
    <nav class="header__nav">
      <a href="#" class="header__nav-item">Home</a>
      <a href="#" class="header__nav-item">About</a>
      <a href="#" class="header__nav-item">Contact</a>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderLayout",
};
</script>

<style lang="scss">
$box-shadow-color: #e0e0e0;

.header {
  background-color: $primary-color;
  padding: 20px;
  box-shadow: 0px 5px 10px $box-shadow-color;
  @include flex-center;
  w &__nav {
    @include flex-center;
  }

  &__nav-item {
    color: $secondary-color;
    padding: 10px;
    text-decoration: none;
    transition: background-color 0.2s ease;

    &:hover {
      color: $primary-color;
      background-color: $secondary-color;
    }
  }
}
</style>
