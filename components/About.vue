<template>
  <section class="about">
    <div class="about__content">
      <h2 class="about__title">About Bio-Fair 2k25</h2>
      <p class="about__text">
        Bio-Fair 2k25 is a national-level technical event organized by the
        Department of Biotechnology, College of Engineering and Technology,
        Bhubaneswar. It aims to bring together students, researchers, and
        industry professionals to explore the latest advancements and
        innovations in the field of biotechnology.
      </p>
      <p class="about__text">
        Join us for an exciting array of workshops, paper presentations, poster
        competitions, and guest lectures from eminent personalities in the
        biotechnology sector. This event provides a unique platform for
        networking, knowledge sharing, and fostering scientific temperament
        among participants.
      </p>
      <p class="about__text">
        We invite you to be a part of this grand celebration of biotechnology
        and contribute to shaping the future of this dynamic field.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
}
</script>

<style lang="scss" scoped>
.about {
  padding: 80px 10vw;
  color: #fff;
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 5; /* Ensure it's above the canvas but below header/footer if they overlap */
  text-align: center;

  &__content {
    max-width: 900px;
    margin: 0 auto;
  }

  &__title {
    font-family: var(--font-family-serif);
    font-size: 3em;
    margin-bottom: 30px;
    color: #1954ec; /* Matching the blue gradient from the title */
    text-shadow: 0 0 15px rgba(25, 84, 236, 0.5);
  }

  &__text {
    font-size: 1.1em;
    line-height: 1.6;
  }
}
</style>
