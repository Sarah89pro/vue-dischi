<template>
    <section class="container album">
        <div class="cards">
            <MainAlbums/>
        </div>

    </section>
</template>

<script>
import axios from 'axios';
import MainAlbums from '../components/MainAlbums';

export default {
    name: 'Main',
    components: {
        MainAlbums,
    },
    data() {
        return {
            apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
            albumList: [],
            loading: true,
        }
    },
    created() {

    },
    methods: {
        getAlbums() {
            /*API CALL */
            axios
                .get(this.apiURL)
                .then(res => {
                    this.albumList = res.data
                })
                .catch(err => {
                    console.log('Error', err);
                });
            this.loading = false;
        }   
    }

};
</script>

<style scoped lang="scss">

</style>