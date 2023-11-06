<script setup lang="ts">
import type { VideoItem } from '@/types/video'

const { data:channelData } = await useFetch('/api/channel') as any
const { data:videoData } = await useFetch('/api/video') as any
console.log(channelData)
console.log(videoData)

</script>

<template>
  <!-- 公共头部 -->
  <app-header/>
  <!-- 频道模块 -->
  <van-tabs>
    <van-tab v-for="item in channelData" :key="item.id" :title="item.name" />
  </van-tabs>
  <!-- 视频列表 -->
  
  <div class="video-list">
    <app-video class="video-list" apiLink="@/api/video"/>
  </div>
</template>

<style lang="scss" scoped>
// 视频列表
.video-list {
  display: flex;
  flex-wrap: wrap;
  padding: 10px 5px;
}
</style>