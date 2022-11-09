<template>
    <div class="flex flex-col card-container items-center pt-4 cursor-pointer basis-1/2 justify-between">
        <div class="flex flex-col">
            <img :src="imgUrl" alt="" class="mx-auto">
            <p class="content mt-5 mx-4">{{ content }}</p>
        </div>
        <p class="footer py-2 mt-8">{{ footer }}</p>
    </div>
</template>

<script>
export default {
    props: {
        imgUrl: String,
        content: String,
        footer: String,
    }
}
</script>

<style lang="scss" scoped>
.card-container {
    background: #FFFFFF;
    box-shadow: 0px 0px 24px rgba(30, 30, 30, 0.15);
    border-radius: 10px;

    &:hover {
        .footer {
            background-color: #1E1E1E;
            color: white;
        }
    }
}

.content {
    font-size: 10px;
    font-weight: 500;
    color: rgba(30, 30, 30, 0.5);
}

.footer {
    width: 100%;
    font-size: 12px;
    font-weight: 600;
    color: #1E1E1E;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
    text-align: center;
}
</style>