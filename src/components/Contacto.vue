<script lang="ts" setup></script>

<style lang="scss" scoped>
  #contacto {
    height: 750px;
    background-color: white;
    position: relative;

    display: flex;
    flex-direction: column;
    align-items: center;

    .title {
      font-size: 50px;
      margin: 75px;
    }

    .content {
      display: flex;
      gap: 100px;

      .adress {
        font-size: 25px;
        margin-bottom: 75px;
        line-height: 1;
      }
    }

    .open {
      width: 100%;
      position: absolute;
      bottom: 0;
      margin-bottom: 650px;
    }
  }
</style>

<template>
  <div id="contacto">
    <div class="open">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path
          fill="white"
          d="M0,192L48,192C96,192,192,192,288,208C384,224,480,256,576,240C672,224,768,160,864,160C960,160,1056,224,1152,240C1248,256,1344,224,1392,208L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
        ></path>
      </svg>
    </div>

    <h2 class="title">Contacte</h2>

    <div class="content">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d2988.255596964875!2d2.1524479!3d41.4987356!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x12a4bde2ffe3aab7%3A0x4a9fbe626d6fc95d!2sMercat%20Municipal%20de%20Ripollet!5e0!3m2!1ses!2ses!4v1747590437346!5m2!1ses!2ses"
        width="600"
        height="400"
        style="border: 0; border-radius: 16px"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>

      <div class="adress">
        <strong>Mercado Municipal de Ripollet</strong> <br /><br />
        Plaça Pere Quart<br />
        08291, Ripollet <br />
        Barcelona, Espanya
      </div>
    </div>
  </div>
</template>
