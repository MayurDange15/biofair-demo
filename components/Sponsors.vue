<template>
  <section class="sponsors">
    <h2 class="sponsors__title">Our Valued Sponsors</h2>
    <div class="sponsors__container">
      <a
        href="#"
        target="_blank"
        rel="noopener noreferrer"
        class="sponsor-logo"
      >
        <img src="./../assets/images/Recon.jpeg" alt="Sponsor One Logo" />
      </a>

      <a
        href="#"
        target="_blank"
        rel="noopener noreferrer"
        class="sponsor-logo"
      >
        <img src="./../assets/images/hero.png" alt="Sponsor Two Logo" />
      </a>

      <a
        href="#"
        target="_blank"
        rel="noopener noreferrer"
        class="sponsor-logo"
      >
        <img src="./../assets/images/prashant.png" alt="Sponsor Three Logo" />
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EventSponsors',
}
</script>

<style lang="scss" scoped>
.sponsors {
  padding: 80px 10vw;
  background-color: rgba(0, 0, 0, 0.7);
  position: relative;
  z-index: 5;
  text-align: center;

  &__title {
    font-family: var(--font-family-serif);
    font-size: 2.5em;
    color: var(--primaryLight);
    margin-bottom: 60px;
    text-shadow: 0 0 15px rgba(25, 84, 236, 0.5);
  }

  &__container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 60px;
    flex-wrap: wrap;
  }
}

.sponsor-logo {
  img {
    max-width: 200px;
    height: auto;
    opacity: 0.8;
    transition: opacity 0.3s ease, transform 0.3s ease;
    filter: brightness(0.9) grayscale(0.5);

    &:hover {
      opacity: 1;
      transform: scale(1.05);
      filter: brightness(1) grayscale(0);
    }
  }
}
</style>
