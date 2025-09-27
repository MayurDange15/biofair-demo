<template>
  <div>
    <Header />
    <Content />
    <Footer />
  </div>
</template>

<script>
import WebGL from '~/webgl'

export default {
  name: 'IndexPage',
  mounted() {
    this.DNA = new WebGL().DNA

    this.initScroll()
  },
  beforeDestroy() {
    window.removeEventListener('wheel', this.handleWheel)
  },
  methods: {
    initScroll() {
      this.handleWheel = (ev) => {
        const delta = ev.deltaY || -ev.wheelDelta
        this.DNA.rotationTarget -= Math.max(Math.min(delta, 40), -40) * 0.01
        // DO NOT prevent default => page will scroll
      }
      window.addEventListener('wheel', this.handleWheel)
    },
  },
}
</script>
