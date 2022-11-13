<template>
    <div class="flex mt-2 card-container cursor-pointer justify-between">
        <div class="grow">
            <p class="name">Desa Margaasih Bandung</p>
            <p class="normal-text">Desa Margaasih Kab. Bandung</p>
            <ButtonView content="Home Visit" />
        </div>
        <div class="flex flex-col justify-center">
            <p class="time-remaining">25 hari lagi</p>
            <p class="normal-text">30 Okt 2022</p>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@mixin text-font($size: 11px, $weight: 400, $color: #1E1E1E) {
    color: $color;

    font: {
        size: $size;
        weight: $weight;
    }
}

.card-container {
    padding: 20px;
    border-radius: 10px;
    background-color: #F3F3F3;
}

.normal-text {
    @include text-font;
}

.name {
    @include text-font(17px, 600, black)
}

.time-remaining {
    @include text-font(11px, 600, #35D0BA)
}
</style>