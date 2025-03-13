<template>
  <van-cell-group inset>
    <van-cell title="分享地址" value="内容1" />
    <van-cell title="分享地址" value="内容2" label="描述信息1" />
  </van-cell-group>
</template>

<route lang="json5">
{
  name: 'share',
  meta: {
    title: '分享',
    i18n: 'menus.share',
    keepAlive: true
  },
}
</route>
