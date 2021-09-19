<template>
  <div class="container">
    <h2 class="title">photography</h2>
    <photo-container class="photo-container" />
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import PhotoContainer from '~/components/photo-container/PhotoContainer.vue'

export default Vue.extend({
  name: 'Photography',
  components: { PhotoContainer }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.title {
  font-family: $cormorant;
}
.container {
  margin: 2vw;
}
</style>
