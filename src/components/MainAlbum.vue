<template>
  <div class="cards">
    <img :src="mainAlbum.poster" :alt="mainAlbum.title">
    <h4> {{ mainAlbum.title }} </h4>
    <h5> {{ mainAlbum.author }} </h5>
    <h5 class="genre"> {{ mainAlbum.year }} </h5>
    <h6> {{ mainAlbum.genre }} </h6>
  </div>
</template>

<script>
export default {
  name: 'MainAlbum',
  props: ['mainAlbum'],
};

</script>

<style scoped lang="scss">
@import '../styles/vars';

.cards {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 1rem;
  height: 380px;
  background: $primary;
}  


.cards img {
  width: 100px;
  height: 100px;
}

h4 {
  text-transform: uppercase;
}

h4,
h6 {
  color: $title;
}


h5 {
  color: $detail;
}

h4,
h5,
h6 {
  margin-top: 12px;
  text-align: center;
}


</style>