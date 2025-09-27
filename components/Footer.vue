<template>
  <footer class="footer">
    <div class="footer__contact">
      <p class="footer__text">Department of Biotechnology</p>
      <p class="footer__text">
        College of Engineering and Technology, Bhubaneswar
      </p>
      <p class="footer__text">BPUT, Odisha, India</p>
      <p class="footer__text">Email: biotech@cet.edu.in</p>
      <p class="footer__text">Phone: +91 1234567890</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
}
</script>

<style lang="scss" scoped>
.footer {
  position: absolute;
  bottom: 0;
  right: 0;
  padding: 20px;
  z-index: 10;
  text-align: right;

  &__contact {
    color: #fff; /* Adjust text color as needed */
  }

  &__text {
    margin: 5px 0;
    font-size: 14px;
    line-height: 1.5;
  }
}
</style>
