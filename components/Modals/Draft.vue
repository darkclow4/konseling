<template>
    <div class="card flex flex-col items-center box-container">
        <img :src="urlImage" alt="" width="180px">
        <p class="card-title my-5 text-center">{{title}}</p>
        <p class="subtitle text-center">{{subtitle}}</p>
        <button @click="$emit('close-modal')">OK</button>
    </div>
</template>

<script>
    export default {
        props: {
            urlImage: String,
            title: String,
            subtitle: String
        }
    }
</script>

<style lang="scss" scoped>
.box-container {
    width: 30vw;
    padding: 40px 70px;
}
button {
    background-color: #1E1E1E;
    color: white;
    padding: 10px;
    border-radius: 10px;
    font-size: 13px;
    font-weight: 500;
    margin-top: 60px;
    width: 30%;
}

.subtitle {
    font-size: 10px;
    font-weight: 500;
    color: rgba(30, 30, 30, 0.5);
}
</style>