<template>
  <header class="header">
    <nuxt-link class="link" to="/">
      <h2 class="title">jayne iris</h2>
    </nuxt-link>
  </header>
</template>

<style lang="scss" scoped>
@import '~assets/styles/config';
.title {
  font-family: $cormorant;
  margin-top: 3vw;
}
.link {
  text-decoration: none;
}
.header {
  @include type(24px, 32px);

  display: flex;
  justify-content: center;
}
</style>
