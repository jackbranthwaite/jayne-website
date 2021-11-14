<template>
  <div class="container">
    <div class="image-container">
      <nuxt-link to="writing" class="title-image-container-one">
        <h2 class="writing">writing</h2>
        <img class="image-one" src="../static/title-one.jpg" />
      </nuxt-link>
      <nuxt-link to="photography" class="title-image-container-two">
        <h2 class="photography">photography</h2>
        <img class="image-two" src="../static/title-two.jpg" />
      </nuxt-link>
    </div>
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
.image-container {
  display: flex;
  justify-content: space-evenly;
}
.writing,
.photography {
  font-family: $cormorant;
  font-size: 24px;
}
img {
  height: auto;
  width: 40vw;
}
.writing {
  margin-left: 6vw;
  margin-top: 4vw;
  position: absolute;
}
.photography {
  margin-left: 3vw;
  margin-top: 20vw;
  position: absolute;
}
/* stylelint-disable */
.title-image-container-one {
  position: relative;
  transform: rotate(-5deg);
  margin-top: -6vw;

  &:hover {
    .image-one {
      opacity: 0.6;
    }
    .writing {
      color: #000;
    }
  }
}
.title-image-container-two {
  position: relative;
  transform: rotate(-2.5deg);
  margin-top: -2vw;
  &:hover {
    .image-two {
      opacity: 0.6;
    }

    .photography {
      color: #000;
    }
  }
}
</style>
