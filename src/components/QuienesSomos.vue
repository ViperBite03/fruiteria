<script lang="ts" setup></script>

<style lang="scss" scoped>
  #nosotros {
    height: 100vh;
    padding: 75px 400px;
    gap: 20px;

    background-color: #f9f8ee;
    background-image: url('dark-bg.png');

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    .title {
      font-size: 50px;
    }

    .content {
      display: flex;
      align-items: center;
      justify-content: center;

      gap: 75px;

      p {
        font-size: 30px;
        width: 600px;
        line-height: 1;
      }

      .blob {
        border-radius: 57% 43% 72% 28% / 36% 55% 45% 64%;
        width: 400px;
        height: 400px;
        overflow: hidden;

        img {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
    }
  }
</style>

<template>
  <div id="nosotros">
    <h2 class="title">¿Qui es Joan?</h2>

    <div class="content">
      <p>
        Joan Pons, l'ànima de la nostra fruiteria, fa anys que dirigeix ​​el seu petit però vibrant negoci al mercat
        local. <br /><br />Al costat del seu dedicat equip de dues persones, ha construït una reputació basada en la
        qualitat i el servei personalitzat, la seva passió per oferir els millors productes frescos i la seva constant
        dedicació. han convertit en un referent al mercat. <br /><br />
        Ara busca evolucionar i modernitzar el seu negoci per continuar oferint el millor servei a la seva comunitat.
      </p>
      <div class="blob">
        <img
          src="https://static.wixstatic.com/media/96b0d9_5e10439fedef4885a2fa4ec9baa8eec9~mv2.jpg/v1/fill/w_640,h_402,al_c,q_80,usm_0.66_1.00_0.01,enc_avif,quality_auto/96b0d9_5e10439fedef4885a2fa4ec9baa8eec9~mv2.jpg"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
