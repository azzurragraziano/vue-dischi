<template>
  <div class="container">
    <div class="loader"></div>
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
        width: 150px;
        height: 150px;
        border-left: 5px solid #ff006e;
        border-radius: 50%;
        animation: rightrotate 900ms linear infinite;
    }

    .loader::before,
    .loader::after {
        content: '';
        width: 120px;
        height: 120px;
        display: block;
        position: absolute;
        top: calc(50% - 50px);
        left: calc(50% - 50px);
        border-right: 4px solid #3a86ff;
        border-radius: 50%;
        animation: leftrotate 900ms linear infinite;
    }

    .loader::after {
        width: 90px;
        height: 90px;
        top: calc(50% - 45px);
        left: calc(50% - 45px);
        border: 0;
        border-left: 3px solid #339922;
        animation: none;
    }

    @keyframes leftrotate {
        from {
            transform: rotate(0deg);
        } to {transform: totate(720deg);}
    }

    @keyframes rightrotate {
        from {
            transform: rotate(360deg);
        } to {transform: totate(0deg);}
    }
</style>