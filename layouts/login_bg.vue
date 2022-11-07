<template>
    <div class="background-img">
        <Nuxt />
    </div>
</template>
   
<style lang="scss">
.background-img {
    width: 100vw;
    height: 100vh;
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("~assets/img/login_bg.png");
    background-size: cover;
    background-attachment: fixed;
    background-repeat: no-repeat;
}
</style>