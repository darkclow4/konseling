<template>
    <div class="flex header-container py-6 px-14">
        <p class="font-semibold text-3xl italic">{{title}}</p>
    </div>
</template>

<script>
    export default {
        computed: {
            title(){
                return this.$route.name === "home" ? "Dashboard" : "Daftar Konseling";
            }
        }
    }
</script>

<style lang="scss" scoped>
.header-container {
    background: white;
    height: 80px;
}
</style>