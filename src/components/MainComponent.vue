<template>
    <section>

        <!-- card container -->
        <div class="container">
            <SingleCardComponent v-for="(element, index) in albums" :key="index" :album="element"/>
        </div>

        <!-- loader -->
        <div class="loader">
            <LoaderComponent v-if="albums.length < 10"/>
        </div>

    </section>
</template> 

<script>
import axios from 'axios';
import SingleCardComponent from './SingleCardComponent.vue';
import LoaderComponent from './LoaderComponent.vue';

export default {
    name:'MainComponent',
    components:{
        SingleCardComponent,
        LoaderComponent
    },
    
    data() {
        return {
            albums:[],
        }
    },
    mounted() {
        setTimeout(() => {
            axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((response)=> {
                this.albums = response.data.response;
            });
        }, 3000)
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables';
    
   .container {
        width: 70%;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        padding-block: 3rem;
   }
</style>