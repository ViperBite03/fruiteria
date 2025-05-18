<script lang="ts" setup>
  interface IProduct {
    name: string
    stock: number
  }

  const productList: IProduct[] = [
    {
      name: 'Manzanas',
      stock: 25,
    },
    {
      name: 'Peras',
      stock: 36,
    },
    {
      name: 'Platanos',
      stock: 48,
    },
    {
      name: 'Naranjas',
      stock: 93,
    },
    {
      name: 'Uvas',
      stock: 13,
    },
    {
      name: 'Fresas',
      stock: 10,
    },
    {
      name: 'Kiwis',
      stock: 20,
    },
    {
      name: 'Mangos',
      stock: 33,
    },
    {
      name: 'Maracuya',
      stock: 8,
    },
  ]
</script>

<style lang="scss" scoped>
  #productos {
    padding: 300px 500px 300px;
    background-color: #f9f8ee;

    background-image: url('/src/assets/dark-bg.png');

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 75px;

    .title {
      font-size: 50px;
    }

    .product-list {
      display: grid;
      gap: 20px;
      grid-template-columns: 200px 200px 200px 200px;

      .product {
        height: 275px;
        padding: 25px 15px;
        border-radius: 16px;
        box-sizing: border-box;

        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;

        background-color: white;

        .product-image {
          width: 100%;
          height: 100%;

          display: flex;
          align-items: center;

          img {
            width: 95%;
            object-fit: contain;
          }
        }

        .details {
          width: 100%;
          padding: 0 20px;
          font-size: 25px;
          box-sizing: border-box;

          display: flex;
          justify-content: space-between;
          align-items: center;

          .stock {
            height: 40px;
            width: 44px;
            border: 1px solid #f8da5b;
            border-radius: 100%;
            padding-top: 4px;

            display: flex;
            align-items: center;
            justify-content: center;
          }
        }
      }
    }
  }
</style>

<template>
  <div id="productos">
    <h2 class="title">Mira el que tenim disponible!</h2>

    <div class="product-list">
      <div class="product" v-for="product in productList">
        <div class="product-image">
          <img :src="`/src/assets/frutas/${product.name}.png`" alt="" />
        </div>
        <div class="details">
          <span class="name">{{ product.name }}</span>
          <span class="stock">{{ product.stock }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
