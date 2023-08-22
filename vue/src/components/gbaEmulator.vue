
<template>
  <div class="gba-container">
    <iframe class="gbaEmulator" src="/gbajs2-master/index.html" scrolling="no"></iframe>
  </div>
</template>

<script>
export default {
  mounted() {
    document.body.classList.add('no-scroll');
  },
  beforeDestroy() {
    document.body.classList.remove('no-scroll');
  }
};
</script>

<style>
.gba-container {
  width: 100vw;
  height: 100vh;
  background: linear-gradient(to bottom, #FFA500, #FF4500);
  overflow: hidden;  /* Hide any overflowing content */
  position: relative;  /* To position the iframe inside it */
}

.gbaEmulator {
  position: absolute;
  top: -10%;  /* This pushes the top part of the iframe content out of view */
  left: 0;
  width: 100%;
  height: 110%;  /* This extends the iframe below the container */
  border: none;
  overflow: hidden;
}
body.no-scroll {
  overflow-y: hidden;
}

</style>