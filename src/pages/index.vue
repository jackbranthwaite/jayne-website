<template>
  <div class="container">
    <img src="../static/title-one.jpg" />
    <img src="../static/title-two.jpg" />
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
