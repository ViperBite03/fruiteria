<script lang="ts" setup>
  interface IProduct {
    name: string
    stock: number
    color: string
    bgColor: string
  }

  const productList: IProduct[] = [
    {
      name: 'Manzanas',
      stock: 3,
      color: '#B21820',
      bgColor: '#d67c80',
    },
    {
      name: 'Peras',
      stock: 3,
      color: 'red',
      bgColor: 'blue',
    },
    {
      name: 'Platanos',
      stock: 3,
      color: '#cc9b88',
      bgColor: '#FEEB87',
    },
    {
      name: 'Naranjas',
      stock: 3,
      color: 'red',
      bgColor: 'blue',
    },
    {
      name: 'Uvas',
      stock: 3,
      color: 'red',
      bgColor: 'blue',
    },
    {
      name: 'Fresas',
      stock: 3,
      color: '#db8181',
      bgColor: '#fcbaba',
    },
    {
      name: 'Kiwis',
      stock: 3,
      color: '#c2db69',
      bgColor: '#E8E9B2',
    },
    {
      name: 'Mangos',
      stock: 3,
      color: '#febb0b',
      bgColor: '#ffe9b2',
    },
    {
      name: 'Maracuya',
      stock: 3,
      color: '#ffc054',
      bgColor: '#af7e82',
    },
  ]
</script>

<style lang="scss" scoped>
  #stock-container {
    padding: 50px 500px;
    background-color: #f9f8ee;

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 75px;

    .title {
      font-size: 40px;
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

        .circle {
          position: relative;

          height: 150px;
          border-radius: 100%;
          aspect-ratio: 1;

          display: flex;
          justify-content: center;
          align-items: center;

          .product-image {
            position: absolute;
            width: 175px;
          }
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
      <div class="product" v-for="product in productList" :style="{ 'background-color': product.bgColor }">
        <div class="circle" :style="{ 'background-color': product.color }">
          <img class="product-image" :src="`src/assets/${product.name}.png`" alt="" />
        </div>
        <div class="details" :style="{ color: product.color }">
          <span class="name">{{ product.name }}</span>
          <span class="stock">{{ product.stock }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
