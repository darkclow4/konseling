<template>
    <div class="card ml-5" style="width: 24vw;">
        <p class="card-title">Komentar Supervisor</p>
        <p class="label-font">Mariansyah</p>
        <p class="label-font">Kamis, 06 Oktober 2022 - 07:22</p>
        <div class="input-container">
            <p class="label-font">Isi Komentar</p>
            <input type="text" value="Bagus, teruskan ke fase berikutnya" disabled>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
input {
    width: 100%;
    background: rgba(30, 30, 30, 0.05);
    border-radius: 10px;
    font-weight: 500;
    font-size: 12px;
    color: #1E1E1E;
    padding: 8px 16px;

    &::placeholder {
        color: rgba(30, 30, 30, 0.3);
    }
}

.label-font {
    font-size: 12px;
    font-weight: 400;
    color: #1E1E1E;
}

.input-container {
    margin-top: 17px;

    p {
        margin-bottom: 6px;
    }
}
</style>