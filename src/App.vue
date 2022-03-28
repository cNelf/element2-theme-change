<template>
  <div id="app">
    <div class="text">主题色本文</div>
    <el-button type="primary">主题色按钮</el-button>
    <div>
      <span>修改主题色：</span>
      <el-color-picker v-model="themeColor" @change="handleChangeTheme" />
    </div>
  </div>
</template>

<script>
  import { changeThemeColor } from './utils/color'

  export default {
    name: 'App',

    data() {
      return {
        themeColor: '#409EFF'
      }
    },

    methods: {
      handleChangeTheme(color) {
        changeThemeColor(color)
      }
    }
  }
</script>

<style lang="scss">
</style>
