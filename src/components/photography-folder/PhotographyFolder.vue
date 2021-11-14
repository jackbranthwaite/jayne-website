<template>
  <div class="photography-folder">
    <button @click="consoleThis">Click Me</button>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'
import { useContext, useAsync } from '@nuxtjs/composition-api'

export default defineComponent({
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
  },
  methods: {
    consoleThis() {
      console.log(this.folders)
    }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';

.photography-folder {
  background-color: $bittersweet;
  height: 200px;
  width: 300px;
}
</style>
