<template>
  <div class="container">
    <h2 class="title">photography</h2>
    <div v-if="folders" class="content-wrapper">
      <div
        v-for="(folder, key) in folders.results"
        :key="key"
        class="folder-container"
      >
        <photography-folder :folder="folder" />
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from '@vue/composition-api'
import { useContext, useAsync } from '@nuxtjs/composition-api'
import PhotographyFolder from '~/components/photography-folder/PhotographyFolder.vue'

export default defineComponent({
  components: { PhotographyFolder },
  setup() {
    const { $prismic } = useContext()

    const folders = useAsync(async () => {
      return await $prismic.api.query(
        $prismic.predicates.at('document.type', 'photography-folder')
      )
    })

    return {
      folders
    }
  }
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
