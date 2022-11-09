<template>
    <div class="flex ml-5 py-2 px-3 button-container items-center cursor-pointer" :style="{backgroundColor:background}">
        <img :src="urlImage" alt="">
        <p class="ml-1 text-xs font-medium text-white">{{content}}</p>
    </div>
</template>

<script>
    export default {
        props: {
            urlImage: String,
            content: String,
            background: String
        }
    }
</script>

<style lang="scss" scoped>
.button-container {
    border-radius: 10px;
}
</style>