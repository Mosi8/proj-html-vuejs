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
    width: 100%;
    img {
        width: 100%;
    }
}
</style>