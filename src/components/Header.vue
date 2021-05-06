<template>
    <header>
        <div class="logo">
        <img src="@/assets/img/logo.png" alt="logo">
        </div>
        
    </header>
  
</template>

<script>

export default {
    name: 'Header',
};

</script>

<style scoped lang="scss">
@import '../styles/vars';
@import '@/styles/general';


header {
    display: flex;
    justify-content: flex-start;
    background-color: $primary;
    height: 65px;
}

.logo {
    width: 45px;
    margin: 10px;
}

.logo img {
    max-width: 100%;
    vertical-align: middle;
}



</style>