<template>
  <div class="card">
        <div class="album-cover">
            <img :src="album.poster" :alt="album.title">
        </div>
        
        <div class="album-info">
            <h3> {{album.title}} </h3>
            <div class="author"> {{album.author}} </div>
            <div class="year"> {{album.year}} </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"SingleCardComponent",
    props:{
        album:Object,
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables';

    .card {
        width: calc((100% / 5) - 0.8rem);
        padding: 0.8rem;
        background-color: $secondary_color;
        margin: 0.8rem 0.4rem;

        .album-cover {
            aspect-ratio: 1/1;

            img {
                height: 100%;
                object-fit: cover;
            }
        }
    }

    .album-info {
        text-align: center;

        h3 {
            margin-block: 0.8rem;
            font-size: 1.15rem;
            text-transform: uppercase;
            color: white;
        }
            > div {
                color: gray;
            }
    }
</style>
