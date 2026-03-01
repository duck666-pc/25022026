<script setup lang="ts">
import router from '@/router';
import { RouterLink } from 'vue-router';

</script>

<template>
    <div>
        <a-menu mode="horizontal">
          <a-menu-item key="trangChu">
            <router-link to="">Trang chủ</router-link>
          </a-menu-item>
          <a-menu-item key="pages">
            <router-link to="">Pages</router-link>
          </a-menu-item>
        </a-menu>   
    </div>
</template>

<script setup></script>
<style scoped></style>