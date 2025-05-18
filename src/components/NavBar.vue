<script setup lang="ts">
  interface IMenuItem {
    href: string
    title: string
    dropdown?: IMenuItem[]
  }

  const items: IMenuItem[] = [
    {
      href: '#stock-container',
      title: 'Element 1',
    },
    {
      href: '#section-container',
      title: 'Element 2',
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

    .items {
      display: flex;
      background-color: #f8f398;
      border-radius: 100px;

      .item-group {
        position: relative;
        padding: 10px;

        &:hover .dropdown {
          display: flex;
        }

        .item {
          color: var(--colorText);

          &:hover {
            color: var(--colorBrand);
          }
        }
      }
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
