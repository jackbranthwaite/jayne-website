<template>
  <div v-if="folder" class="project-container">
    <div v-if="content" class="another-one">
      <div
        v-for="(image, key) in content.body[0].items"
        :key="key"
        class="content-container"
      >
        <img
          :key="key"
          :src="image.folder_content.url"
          :alt="image.folder_content.alt"
          class="contents"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { useAsync, useContext, useRoute } from '@nuxtjs/composition-api'
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup() {
    const route = useRoute()
    const folderId = route.value.params.id

    const { $prismic } = useContext()

    const folder = useAsync(async () => {
      return await $prismic.api.query(
        $prismic.predicates.at('document.id', folderId)
      )
    })

    const content = folder.value?.results[0].data

    return {
      folder,
      content
    }
  }
})
</script>

<style lang="scss" scoped>
.contents {
  height: 100px;
  width: 100px;
}
</style>
