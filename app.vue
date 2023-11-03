<script setup lang="ts">
// SEO Optimization
useSeoMeta({
  title: '哔哩哔哩 (゜-゜)つロ 干杯~-bilibili',
  description: '哔哩哔哩（bilibili.com)是国内知名的视频弹幕网站，这里有及时的动漫新番，活跃的ACG氛围，有创意的Up主。大家可以在这里找到许多欢乐。'
})
</script>

<template>
  <div>
    <nuxt-link to="/">Home</nuxt-link><span>__</span>
    <nuxt-link to="/video">Video</nuxt-link>
    <nuxt-page/>
  </div>
</template>

<style lang="scss">
// 基础样式
@import './assets/styles/base.scss';
// 字体图标
@import './assets/styles/iconfont.scss';

:root {
  /*设置主题色*/
  --van-primary-color: #FB7299 !important;
  --van-back-top-background: #fbfbfb !important;
  --van-back-top-text-color: #666 !important;
}
</style>
