<script setup lang="ts">
const email = ref<string>('')
</script>

<template>
  <van-grid>
    <van-grid-item icon="photo-o" text="文字" dot />
    <van-grid-item icon="photo-o" text="文字" />
    <van-grid-item icon="photo-o" text="文字" />
    <van-grid-item icon="photo-o" text="文字" />
  </van-grid>

  <van-row align="center">
    <van-col span="12" class="h-100 bg-red text-center leading-100">
      S
    </van-col>
    <van-col span="12" class="h-50 bg-blue">
      <div class="v-center text-center">
        QD<br>QD
      </div>
    </van-col>
  </van-row>
  <van-row align="center">
    <van-col span="8" class="h-100 bg-green text-center leading-100">
      S
    </van-col>
    <van-col span="8" class="h-50 bg-bluegray text-center leading-50">
      Q
    </van-col>

    <van-col span="8" class="h-50 bg-blue text-center leading-50">
      <van-row class="h-25 leading-25">
        <van-col span="24" class="bg-green">
          D
        </van-col>
      </van-row>

      <van-row class="h-25 leading-25">
        <van-col span="12" class="bg-red">
          d11111
        </van-col>
        <van-col span="12" class="bg-coolGray">
          d2
        </van-col>
      </van-row>
    </van-col>
  </van-row>
  <van-cell-group inset>
    <van-cell title="分享地址" value="内容1" />
    <van-cell title="分享地址" value="内容2" label="描述信息1" />
    <van-field v-model="email" type="email" placeholder="请输入邮箱" label="邮箱" required />
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
