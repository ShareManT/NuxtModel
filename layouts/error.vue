<style lang="scss">
</style>

<template>
  <LayoutContainer>
    <h1 v-if="error.statusCode === 404">
      页面不存在
    </h1>
    <h1 v-else>
      应用发生错误异常
    </h1>
    <nuxt-link to="/">
      首页
    </nuxt-link>
  </LayoutContainer>
</template>
