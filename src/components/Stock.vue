<script lang="ts" setup>
  interface IProduct {
    name: string
    stock: number
  }

  const productList: IProduct[] = [
    {
      name: 'Manzanas',
      stock: 3,
    },
    {
      name: 'Peras',
      stock: 3,
    },
    {
      name: 'Platanos',
      stock: 3,
    },
    {
      name: 'Naranjas',
      stock: 3,
    },
    {
      name: 'Uvas',
      stock: 3,
    },
    {
      name: 'Fresas',
      stock: 3,
    },
    {
      name: 'Kiwis',
      stock: 3,
    },
    {
      name: 'Mangos',
      stock: 3,
    },
    {
      name: 'Maracuya',
      stock: 3,
    },
  ]
</script>

<style lang="scss" scoped>
  #stock-container {
    padding: 300px 500px;
    background-color: #f9f8ee;

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
        height: 250px;
        padding: 20px 0;
        border-radius: 16px;

        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;

        background-color: white;

        .product-image {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }

        .details {
          background-color: white;
          padding: 5px 10px;
          border-radius: 8px;

          display: flex;
          gap: 20px;
        }
      }
    }
  }
</style>

<template>
  <div id="stock-container">
    <h2 class="title">Mira el que tenim disponible!</h2>

    <div class="product-list">
      <div class="product" v-for="product in productList">
        <img class="product-image" :src="`src/assets/${product.name}.png`" alt="" />
        <div class="details">
          <span class="name">{{ product.name }}</span>
          <span class="stock">{{ product.stock }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
