<template>
  <div class="logo">
      <img :src="immagine">
  </div>
</template>

<script>
export default {
    name: 'Logo',
    props: {
        immagine: String
    }

}
</script>

<style lang="scss" scoped>

.logo {
    height: 100%;
    img {
        height: 100%;
    }
}
</style>