<script setup lang="ts">
import { routeWhiteList } from '@/config/routes'

const { t } = useI18n()
const active = ref(0)
const route = useRoute()

const show = computed(() => route.name && routeWhiteList.includes(route.name))
</script>

<template>
  <van-tabbar v-if="show" v-model="active" placeholder route>
    <van-tabbar-item replace to="/share">
      {{ t('layouts.share') }}
      <template #icon>
        <div class="i-carbon:share" />
      </template>
    </van-tabbar-item>
    <van-tabbar-item replace to="/product">
      {{ t('layouts.product') }}
      <template #icon>
        <div class="i-carbon:product" />
      </template>
    </van-tabbar-item>
    <van-tabbar-item replace to="/exchange">
      {{ t('layouts.exchange') }}
      <template #icon>
        <div class="i-carbon:chart-line" />
      </template>
    </van-tabbar-item>

    <van-tabbar-item replace to="/user">
      {{ t('layouts.user') }}
      <template #icon>
        <div class="i-carbon:user" />
      </template>
    </van-tabbar-item>
  </van-tabbar>
</template>
