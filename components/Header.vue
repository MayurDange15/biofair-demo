<template>
  <header class="header">
    <img
      src="./../assets/images/logo.png"
      alt="Bio-Fair 2k25 Banner"
      class="header__banner"
    />
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<style lang="scss" scoped>
.header {
  position: absolute;
  top: 0;
  left: 0;
  //   width: 100%;
  display: flex;
  justify-content: normal;
  padding: 20px;
  z-index: 10;

  &__banner {
    max-width: 50%; /* Adjust as needed */
    height: auto;
  }
}
</style>
