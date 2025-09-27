<template>
  <section class="guests">
    <h2 class="guests__title">Meet Our Honorable Guests</h2>
    <div class="guests__container">
      <div class="guest-card">
        <img
          src="./../assets/images/Kashyap.png"
          alt="Profile picture of Guest 1"
          class="guest-card__img"
        />
        <h3 class="guest-card__name">Dr. Rajpal Singh Kashyap</h3>
        <p class="guest-card__title">
          Director, Advanced Research Centre, Central India Institute of Medical
          Sciences, Nagpur
        </p>
        <p class="guest-card__bio">
          His areas of research interest are Immunology and Molecular
          Diagnostics, Proteomics, Neurology, Neurosciences and Infectious
          diseases, including Tuberculosis, Brain TB, Chikungunya, Neuroviruses,
          Bacterial Meningitis, Neurozoonotic and Covid-19 infections. He is
          currently working on various research projects which include
          prevalence of Zoonotic infections in Central India, Role of Herbal
          Drugs in Infectious and Noninfectious diseases, Strategy for Booster
          BCG vaccination, Diagnosis of active and latent TB.
        </p>
      </div>

      <div class="guest-card">
        <img
          src="./../assets/images/Rahul.png"
          alt="Profile picture of Guest 2"
          class="guest-card__img"
        />
        <h3 class="guest-card__name">Mr. Rahul Satpute</h3>
        <p class="guest-card__title">Founder And CEO at Bhumitra Lab Pvt Ltd</p>
        <p class="guest-card__bio">
          Experienced Founder with a demonstrated history of working in the
          biotechnology industry. Skilled in Customer Service, Strategic
          Planning, Marketing, Sales, Social Media, and Environmental Awareness.
          Strong business development professional with a Masters in Rural
          Development and Psychology focused in Rural Sociology from Indira
          Gandhi National Open University.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HonorableGuests',
}
</script>

<style lang="scss" scoped>
.guests {
  padding: 80px 10vw;
  background-color: var(--black);
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
    gap: 40px;
    flex-wrap: wrap;
    max-width: 900px;
    margin: 0 auto;
  }
}

.guest-card {
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 10px;
  padding: 30px;
  width: 300px;
  border: 1px solid rgba(25, 84, 236, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;

  &:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(25, 84, 236, 0.2);
  }

  &__img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 3px solid var(--primaryLight);
    margin-bottom: 20px;
  }

  &__name {
    margin: 0;
    font-size: 1.5em;
    color: #fff;
  }

  &__title {
    margin: 5px 0 15px 0;
    color: rgba(255, 255, 255, 0.7);
    font-weight: 300;
  }

  &__bio {
    font-size: 0.9em;
    line-height: 1.6;
    color: rgba(255, 255, 255, 0.8);
  }
}
</style>
