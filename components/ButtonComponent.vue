<template>
    <div @click="$emit('click')" class="flex ml-5 py-2 px-3 button-container items-center cursor-pointer" :style="{backgroundColor:background}">
        <img :src="urlImage" alt="" width="18px">
        <p class="ml-1 text-xs font-medium text-white">{{content}}</p>
    </div>
</template>

<script>
    export default {
        props: {
            urlImage: String,
            content: {
                type: String,
                default: ""
            },
            background: String
        }
    }
</script>

<style lang="scss" scoped>
.button-container {
    border-radius: 10px;
}
</style>