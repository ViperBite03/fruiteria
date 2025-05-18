<script lang="ts" setup></script>

<style lang="scss" scoped>
  #inicio {
    height: 100vh;
    background-color: #f9f8ee;

    background-image: url('dark-bg.png');

    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 75px;
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

      .redirect {
        transition: 0.3s ease;
        width: fit-content;

        border-radius: 100px;
        border: none;
        padding: 3px 20px 0px;

        background-color: white;
        font-size: 25px;

        &:hover {
          background-color: #f8da5b;
          color: white;
        }
      }
    }

    a {
      text-decoration: none;
      color: black;
    }
  }
</style>

<template>
  <div id="inicio">
    <div class="left">
      <p class="title">
        Disfruta de la millor<br />
        varietat de fruita, <br />del mercat a casa teva!
      </p>
      <a class="redirect" href="#productos">Vine a visitar-nos!</a>
    </div>

    <img
      src="https://png.pngtree.com/png-clipart/20240903/original/pngtree-falling-lemon-fruit-realistic-illustration-png-image_15929673.png"
      alt=""
    />
  </div>
</template>
