<template>

  <section class="main">
    
    <div v-if="!loading" class="container music">
      <div v-for="(album, index) in albumList" :key="index" class="cards">
        <MainAlbum :mainAlbum="album" />
      </div>
    </div>
    <div v-else class="loader">LOADING</div>
    
  </section>
</template>

<script>

import axios from 'axios';

import MainAlbum from '@/components/MainAlbum.vue';

export default {
  name: "Main",
  components: {
    
    MainAlbum,
  },
  data() {
    return {
      apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
      albumList: [],
      
      loading: true,
    };
  },
  created() {
    this.getAlbums();
  },
  methods: {
    
    getAlbums() {
      axios
        .get(this.apiURL)
        .then((res) => {
          this.albumList = res.data.response;
          this.loading = false;
        })
        .catch((err) => {
          console.log("Error", err);
        });
    },
    
  },

  
};


</script>

<style scoped lang="scss">
@import '../styles/vars';

.main {
    height: calc(100vh - 65px);
}


.music {
    display: flex;
    flex-wrap: wrap;
    margin-top: 16px;
    justify-content: center;

}


.cards {
    display: flex;
    flex-basis: calc(100% / 8);
    margin-top: 10px;
}

</style>