<script setup lang="ts">
  interface IMenuItem {
    href: string
    title: string
    dropdown?: IMenuItem[]
  }

  const items: IMenuItem[] = [
    {
      href: '#section-container',
      title: 'Inicio',
    },
    {
      href: '#stock-container',
      title: 'Productos',
    },
    {
      href: '#stock-container',
      title: 'Quienes somos',
    },
  ]

  import { ref } from 'vue'
  const open = ref(false)
</script>

<style lang="scss" scoped>
  .menu {
    position: fixed;
    z-index: 7;
    height: 50px;
    width: 100%;

    display: flex;
    align-items: center;
    justify-content: center;
    padding: 50px;

    font-size: 25px;

    .items {
      display: flex;
      background-color: white;
      gap: 10px;
      padding: 10px;
      border-radius: 100px;

      .item-group {
        border-radius: 200px;
        background-color: #f9f8ee;
        position: relative;
        padding: 3px 15px 0px;

        transition: 0.3s ease;

        &:hover {
          background-color: #f8f398;

          a {
            color: black;
          }
        }
      }
    }

    a {
      transition: 0.3s ease;
      text-decoration: none;
      color: rgb(143, 143, 143);
    }
  }
</style>

<template>
  <div class="menu">
    <div class="items">
      <div class="item-group" v-for="item in items" :key="item.title">
        <a class="item" :href="item.href" :title="item.title">
          {{ item.title }}
        </a>
      </div>
    </div>
  </div>
</template>
