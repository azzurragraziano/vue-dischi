<template>
  <div class="container">
    <div class="loader">
        <h4>caricamento...</h4>
    </div>
  </div>
</template>

<script>
export default {
    name: "LoaderComponent"
}
</script>

<style lang="scss" scoped>
    .loader {
        margin: 0 auto;
    
        h4 {
            color: white;
            font-size: 2rem;
            font-weight: bold;
        }
    }

</style>