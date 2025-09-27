<!-- <template>
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
</style> -->
<!-- <template>
  <footer class="footer">
    <div class="footer__main">
      <div class="footer__section">
        <h4 class="footer__title">Contact Us</h4>
        <p>Department of Biotechnology</p>
        <p>College of Engineering and Technology, Bhubaneswar</p>
        <p>BPUT, Odisha, India</p>
        <p>Email: biotech@cet.edu.in</p>
        <p>Phone: +91 1234567890</p>
      </div>

      <div class="footer__section">
        <h4 class="footer__title">Honorable Guests</h4>
        <div class="footer__person">
          <p class="footer__person-name">Dr. Jane Doe</p>
          <p class="footer__person-title">Lead Scientist, BioInnovate Inc.</p>
        </div>
        <div class="footer__person">
          <p class="footer__person-name">Prof. John Smith</p>
          <p class="footer__person-title">
            Head of Genetics, National University
          </p>
        </div>
      </div>

      <div class="footer__section">
        <h4 class="footer__title">Our Sponsors</h4>
        <div class="footer__sponsors">
          <a href="#" target="_blank" rel="noopener noreferrer">
            <img
              src="https://via.placeholder.com/150x60.png?text=Sponsor+One"
              alt="Sponsor One Logo"
              class="footer__sponsor-logo"
            />
          </a>
          <a href="#" target="_blank" rel="noopener noreferrer">
            <img
              src="https://via.placeholder.com/150x60.png?text=Sponsor+Two"
              alt="Sponsor Two Logo"
              class="footer__sponsor-logo"
            />
          </a>
        </div>
      </div>
    </div>

    <div class="footer__bottom">
      <p>Made with ❤️ by Mayur</p>
      <p>&copy; 2025 Bio-Fair. All Rights Reserved.</p>
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
  // We remove 'position: absolute' so the footer sits at the end of the page content.
  position: relative;
  z-index: 5;
  background-color: #111; // A slightly darker shade for contrast
  color: rgba(255, 255, 255, 0.8);
  padding: 60px 10vw 0; // Add padding top and sides, bottom padding is handled by the bottom bar
  font-size: 16px;

  &__main {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap; // Allows sections to stack on smaller screens
    gap: 40px; // Space between sections
    padding-bottom: 40px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }

  &__section {
    flex: 1; // Allows sections to grow and share space
    min-width: 250px; // Prevents sections from getting too squished
  }

  &__title {
    font-family: var(--font-family-serif);
    color: #fff;
    font-size: 1.5em;
    margin-bottom: 20px;
    position: relative;

    // Underline effect for the title
    &::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 40px;
      height: 2px;
      background-color: var(--primaryLight);
    }
  }

  p {
    margin: 10px 0;
    line-height: 1.6;
  }

  &__person {
    margin-bottom: 15px;
  }

  &__person-name {
    font-weight: bold;
    color: #fff;
    margin: 0;
  }

  &__person-title {
    font-size: 0.9em;
    color: rgba(255, 255, 255, 0.7);
    margin: 5px 0 0 0;
  }

  &__sponsors {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  &__sponsor-logo {
    max-width: 150px;
    height: auto;
    opacity: 0.8;
    transition: opacity 0.3s ease;

    &:hover {
      opacity: 1;
    }
  }

  &__bottom {
    padding: 20px 0;
    text-align: center;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.6);

    p {
      margin: 5px 0;
    }
  }
}
</style> -->
<template>
  <footer class="footer">
    <div class="footer__main">
      <h4 class="footer__title">Contact Us</h4>
      <p>Department of Biotechnology</p>
      <p>
        Tulsiramji Gaikwad-Patil College of Engineering and Technology, Nagpur
      </p>
      <p>Nagpur, Maharashtra, India</p>
      <p>Email: hod.bt@tgpcet.com | Phone: +91 9096899826</p>
    </div>

    <div class="footer__bottom">
      <p>Made with ❤️ by Mayur</p>
      <p>&copy; 2025 Bio-Fair. All Rights Reserved.</p>
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
  position: relative;
  z-index: 5;
  background-color: #111;
  color: rgba(255, 255, 255, 0.8);
  padding: 40px 10vw 0;
  text-align: center;

  &__main {
    padding-bottom: 30px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }

  &__title {
    font-family: var(--font-family-serif);
    color: #fff;
    font-size: 1.5em;
    margin-bottom: 20px;
  }

  p {
    margin: 10px 0;
    line-height: 1.6;
    font-size: 16px;
  }

  &__bottom {
    padding: 20px 0;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.6);

    p {
      margin: 5px 0;
    }
  }
}
</style>
