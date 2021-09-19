<template>
  <div class="container">
    <div class="test"></div>
    <div class="test"></div>
    <div class="test"></div>
    <div class="test"></div>
    <div class="test"></div>
    <div class="test"></div>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup() {}
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  align-content: center;
  display: grid;
  gap: 20px;
  grid-template-columns: 1fr 1fr 1fr;
}
.test {
  background-color: $bittersweet;
  height: 200px;
  width: 300px;
}
</style>
