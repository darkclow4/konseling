<template>
    <div class="background-img">
        <Nuxt />
    </div>
</template>
   
<style lang="scss">
.background-img {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("~assets/img/login_bg.png");
    background-size: cover;
    background-attachment: fixed;
    background-repeat: no-repeat;
}
</style>