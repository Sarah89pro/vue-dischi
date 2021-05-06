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

header {
    display: flex;
    justify-content: flex-start;
    background-color: #2E3A46;
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


@import '@/styles/general';

</style>