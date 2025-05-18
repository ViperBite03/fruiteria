<script lang="ts" setup></script>

<style lang="scss" scoped>
  #section-container {
    position: relative;
    padding: 100px 500px;

    .open {
      width: 100%;
      position: absolute;
      bottom: 0;
    }

    .title {
      font-size: 50px;
    }
  }
</style>

<template>
  <div id="section-container">
    <div class="open">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path
          fill="black"
          d="M0,192L48,192C96,192,192,192,288,208C384,224,480,256,576,240C672,224,768,160,864,160C960,160,1056,224,1152,240C1248,256,1344,224,1392,208L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
        ></path>
      </svg>
    </div>
    <h2 class="title">Quienes somos</h2>
  </div>
</template>
