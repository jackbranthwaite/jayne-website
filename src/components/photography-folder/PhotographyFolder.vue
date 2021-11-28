<template>
  <div v-if="folder" class="photography-folder">
    <button @click="conThis(folder)">Click</button>
    <nuxt-link :to="`photography/folder/${folder.id}`">
      <img
        :src="folder.data.header_image.url"
        alt="folder main image"
        class="main-image"
      />
      <p class="folder-title">{{ folder.data.title }}</p>
    </nuxt-link>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  props: {
    folder: {
      type: Object,
      default: () => {}
    }
  },
  setup() {},
  methods: {
    conThis(folder) {
      console.log(folder)
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.main-image {
  height: auto;
  min-width: 500px;
  width: 5vw;
}
</style>
