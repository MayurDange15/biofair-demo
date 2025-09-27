<template>
  <section class="cta">
    <div class="cta__content">
      <h2 class="cta__title">Ready to Join the Future of Biotechnology?</h2>
      <p class="cta__subtitle">
        Secure your spot at Bio-Fair 2k25. Don't miss this opportunity to learn,
        network, and innovate.
      </p>
      <a
        href="https://docs.google.com/forms/d/e/1FAIpQLSdQ58qLrH-ia9U2YLVZlegeBjZf8jSaOU22jgutC3B5H82B0Q/viewform"
        class="cta__button"
        >Register Now</a
      >
    </div>
  </section>
</template>

<script>
export default {
  name: 'RegisterCTA',
}
</script>

<style lang="scss" scoped>
.cta {
  padding: 100px 10vw;
  position: relative;
  z-index: 5;
  background: radial-gradient(circle, #1954ec22, var(--black) 70%);
  text-align: center;
  overflow: hidden;

  &__content {
    max-width: 800px;
    margin: 0 auto;
  }

  &__title {
    font-family: var(--font-family-serif);
    font-size: 3em;
    color: #fff;
    margin-bottom: 20px;
    text-shadow: 0 0 20px rgba(25, 84, 236, 0.5);
  }

  &__subtitle {
    font-size: 1.2em;
    color: rgba(255, 255, 255, 0.8);
    margin-bottom: 40px;
    line-height: 1.6;
  }

  &__button {
    display: inline-block;
    padding: 15px 40px;
    font-size: 1.2em;
    font-weight: bold;
    color: #fff;
    background-color: var(--primaryLight);
    border: none;
    border-radius: 50px;
    text-decoration: none;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease,
      background-color 0.3s ease;
    box-shadow: 0 0 25px rgba(25, 84, 236, 0.7);

    // Remove the default underline from the global 'a' styles
    &::after {
      display: none;
    }

    &:hover {
      transform: scale(1.05) translateY(-5px);
      box-shadow: 0 0 40px rgba(25, 84, 236, 1);
      background-color: #2b6aff; // A slightly brighter blue on hover
    }
  }
}
</style>
