<script lang="ts" setup></script>

<style lang="scss" scoped>
  #section-container {
    height: 100vh;
    background-color: #f9f8ee;

    display: flex;
    align-items: center;
    justify-content: center;
    gap: 200px;

    img {
      height: 600px;
    }

    .left {
      display: flex;
      flex-direction: column;
      gap: 20px;

      .title {
        font-size: 60px;
        margin: 0;
        line-height: 1;
      }

      button {
        font-family: 'Dongle', sans-serif;
        width: fit-content;

        border-radius: 100px;
        border: none;
        padding: 3px 20px 0px;

        background-color: white;
        font-size: 25px;
      }
    }
  }
</style>

<template>
  <div id="section-container">
    <div class="left">
      <p class="title">
        Disfruta de la millor<br />
        varietat de fruita, <br />del mercat a casa teva!
      </p>
      <button>Ver nuestros productos</button>
    </div>

    <img
      src="https://png.pngtree.com/png-clipart/20240903/original/pngtree-falling-lemon-fruit-realistic-illustration-png-image_15929673.png"
      alt=""
    />
  </div>
</template>
