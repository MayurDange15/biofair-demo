<template>
  <section class="countdown">
    <h2 class="countdown__title">The Event Begins In</h2>
    <div v-if="!hasEnded" class="countdown__timer">
      <div class="countdown__block">
        <span class="countdown__value">{{ days }}</span>
        <span class="countdown__label">Days</span>
      </div>
      <div class="countdown__block">
        <span class="countdown__value">{{ hours }}</span>
        <span class="countdown__label">Hours</span>
      </div>
      <div class="countdown__block">
        <span class="countdown__value">{{ minutes }}</span>
        <span class="countdown__label">Minutes</span>
      </div>
      <div class="countdown__block">
        <span class="countdown__value">{{ seconds }}</span>
        <span class="countdown__label">Seconds</span>
      </div>
    </div>
    <div v-else class="countdown__ended">
      <h3 class="countdown__ended-message">The event is happening now!</h3>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EventCountdown',
  data() {
    return {
      // IMPORTANT: Change this to your event's start date and time!
      // Format: YYYY-MM-DDTHH:MM:SS
      targetDate: '2025-09-29T12:00:00',
      days: 0,
      hours: 0,
      minutes: 0,
      seconds: 0,
      timerInterval: null,
      hasEnded: false,
    }
  },
  mounted() {
    this.startCountdown()
  },
  beforeDestroy() {
    // Clear the interval when the component is destroyed to prevent memory leaks
    clearInterval(this.timerInterval)
  },
  methods: {
    startCountdown() {
      const countDownDate = new Date(this.targetDate).getTime()

      this.timerInterval = setInterval(() => {
        const now = new Date().getTime()
        const distance = countDownDate - now

        if (distance < 0) {
          clearInterval(this.timerInterval)
          this.hasEnded = true
          return
        }

        this.days = Math.floor(distance / (1000 * 60 * 60 * 24))
        this.hours = Math.floor(
          (distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
        )
        this.minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
        this.seconds = Math.floor((distance % (1000 * 60)) / 1000)
      }, 1000)
    },
  },
}
</script>

<style lang="scss" scoped>
.countdown {
  padding: 80px 10vw;
  text-align: center;
  position: relative;
  z-index: 5;
  background-color: rgba(0, 0, 0, 0.5); // A bit more subtle background

  &__title {
    font-family: var(--font-family-serif);
    font-size: 2.5em;
    color: var(--primaryLight);
    margin-bottom: 40px;
    text-shadow: 0 0 15px rgba(25, 84, 236, 0.5);
  }

  &__timer {
    display: flex;
    justify-content: center;
    gap: 30px;
  }

  &__block {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: rgba(25, 84, 236, 0.1);
    padding: 20px;
    border-radius: 10px;
    border: 1px solid rgba(25, 84, 236, 0.3);
    min-width: 120px;
  }

  &__value {
    font-size: 3em;
    font-weight: bold;
    color: #fff;
    line-height: 1;
  }

  &__label {
    font-size: 1em;
    color: rgba(255, 255, 255, 0.7);
    margin-top: 10px;
  }

  &__ended-message {
    font-size: 2em;
    color: #fff;
    text-shadow: 0 0 10px var(--primaryLight);
  }
}
</style>
