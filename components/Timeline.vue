<template>
  <section class="timeline">
    <h2 class="timeline__title">Event Schedule</h2>
    <div class="timeline__container">
      <div v-for="day in schedule" :key="day.day">
        <h3 class="timeline__day-title">Day {{ day.day }}</h3>
        <!-- <h3 class="timeline__day-title">Day {{ dayIndex.day }}</h3> -->
        <div v-for="item in day.events" :key="item.time" class="timeline__item">
          <!-- <h3 class="timeline__day-title">Day {{ itemIndex }}</h3> -->
          <div class="timeline__content">
            <span class="timeline__time">{{ item.time }}</span>
            <h4 class="timeline__event-title">{{ item.title }}</h4>
            <p class="timeline__event-description">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EventTimeline',
  data() {
    return {
      // IMPORTANT: You can customize the entire event schedule here.
      schedule: [
        {
          day: 1,
          events: [
            {
              time: '09:00 AM',
              title: 'Registration & Welcome',
              description:
                'Doors open for registration. Welcome kits and coffee.',
            },
            {
              time: '10:00 AM',
              title: 'Inauguration & Keynote',
              description:
                'Opening ceremony followed by a keynote from a leading industry expert.',
            },
            {
              time: '11:30 AM',
              title: 'Paper Presentation Contest',
              description:
                'Students and researchers present their innovative work.',
            },
            {
              time: '01:00 PM',
              title: 'Lunch Break',
              description: 'Networking lunch for all attendees.',
            },
            {
              time: '02:00 PM',
              title: 'Workshop Session 1',
              description: 'Hands-on workshop on CRISPR-Cas9 technology.',
            },
            {
              time: '04:00 PM',
              title: 'Poster Competition',
              description: 'Exhibition and judging of scientific posters.',
            },
          ],
        },
        {
          day: 2,
          events: [
            {
              time: '09:30 AM',
              title: 'Guest Lecture',
              description:
                'An insightful talk on "The Future of Synthetic Biology".',
            },
            {
              time: '11:00 AM',
              title: 'Bio-Quiz Finals',
              description:
                'The final round of the inter-college biotechnology quiz.',
            },
            {
              time: '12:30 PM',
              title: 'Lunch Break',
              description: 'Enjoy a delicious lunch.',
            },
            {
              time: '01:30 PM',
              title: 'Industry Panel Discussion',
              description:
                'A discussion on career paths and opportunities in biotech.',
            },
            {
              time: '03:30 PM',
              title: 'Valedictory & Prize Distribution',
              description: 'Closing ceremony and announcement of winners.',
            },
          ],
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.timeline {
  padding: 80px 10vw;
  position: relative;
  z-index: 5;
  background-color: var(--black);

  &__title {
    text-align: center;
    font-family: var(--font-family-serif);
    font-size: 2.5em;
    color: var(--primaryLight);
    margin-bottom: 60px;
    text-shadow: 0 0 15px rgba(25, 84, 236, 0.5);
  }

  &__container {
    position: relative;
    max-width: 900px;
    margin: 0 auto;

    // The central timeline bar
    &::after {
      content: '';
      position: absolute;
      width: 4px;
      background-color: var(--primaryLight);
      top: 0;
      bottom: 0;
      left: 50%;
      margin-left: -2px;
      box-shadow: 0 0 10px var(--primaryLight);
    }
  }

  &__day-title {
    text-align: center;
    font-size: 2em;
    padding: 20px 0;
    color: #fff;
  }

  &__item {
    padding: 10px 40px;
    position: relative;
    width: 50%;

    // The circle on the timeline bar
    &::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      right: -10px;
      background-color: var(--white);
      border: 4px solid var(--primaryLight);
      top: 25px;
      border-radius: 50%;
      z-index: 1;
    }

    // Items on the left side
    &:nth-child(odd) {
      left: 0;
      padding-right: 70px;
      text-align: right;
    }

    // Items on the right side
    &:nth-child(even) {
      left: 50%;
      padding-left: 70px;
      text-align: left;

      &::after {
        left: -10px;
      }
    }
  }

  &__content {
    padding: 20px;
    background: rgba(255, 255, 255, 0.05);
    border-radius: 6px;
  }

  &__time {
    display: block;
    font-weight: bold;
    color: var(--primaryLight);
    margin-bottom: 8px;
  }

  &__event-title {
    margin: 0 0 10px 0;
    font-size: 1.2em;
    color: #fff;
  }

  &__event-description {
    margin: 0;
    font-size: 0.9em;
    color: rgba(255, 255, 255, 0.8);
    line-height: 1.5;
  }
}
</style>
