<template>
  <div class="container">
    <p class="title">Hello World</p>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Home',
  components: {}
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.title {
  font-family: $cormorant;
}
</style>
