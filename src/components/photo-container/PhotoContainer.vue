<template>
  <div class="photo-container">
    <photography-folder />
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'
import PhotographyFolder from '../photography-folder/PhotographyFolder.vue'

export default defineComponent({
  components: { PhotographyFolder },
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
