<template>
  <header>
    <div class="logo">
        <img src="@/assets/img/logo.png" alt="">
    </div>
  </header>
</template>

<script>
export default {
    name: "HeaderComponent"
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

    header {
        background-color: $secondary_color;

        img {
            width: 50px;
            margin: 0.5rem 0.8rem;
        }
    }

    
</style>