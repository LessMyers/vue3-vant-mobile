<script setup lang="ts">
const email = ref<string>('')

const emailField = ref(null)

// 失去焦点时触发校验
function validateOnBlur() {
  emailField.value.validate()
}

function validator(value: string) {
  if (!value)
    return true // 允许为空
  const emailPattern = /^[\w.%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/i
  return emailPattern.test(value)
}
</script>

<template>
  <van-cell-group inset>
    <van-cell title="分享地址" value="内容1" />
    <van-cell title="分享地址" value="内容2" label="描述信息1" />
    <van-field v-model="email" type="email" placeholder="请输入邮箱" label="邮箱" required />
    <van-field
      ref="emailField"
      v-model="email"
      label="邮箱"
      type="text"
      placeholder="请输入邮箱"
      required
      :rules="[{ validator, message: '请输入正确邮箱' }]"
      @blur="validateOnBlur"
    />
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
