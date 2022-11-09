<template>
    <div class="flex grow p-5">
        <div class="flex flex-col flex-auto">
            <div class="flex basis-1/3">
                <div @click="showModal = true" class="flex flex-col justify-between items-center cursor-pointer card button-card aspect-square mr-5">
                    <img src="~/assets/img/icons/plus.png" alt="" width="80px" height="80px">
                    <p class="w-40 mb-4">Buat Konseling Makro Baru</p>
                </div>
                <div class="flex-auto card">
                    <p class="card-title">Riwayat Konseling</p>
                </div>
            </div>
            <div class="flex basis-2/3 card mt-5">
                <p class="card-title">Quick Access Konseling</p>
            </div>
        </div>
        <div class="flex flex-col card ml-5 right-div">
            <p class="card-title">Jadwal Konseling Terdekat</p>
            <NearlyKonseling />
            <NearlyKonseling />
            <NearlyKonseling />
            <NearlyKonseling />
        </div>
        <ModalsNewKonseling v-show="showModal" @close-modal="showModal = false" />
    </div>
</template>

<script>
export default {
    layout: "dashboard",
    data() {
        return{
            showModal: false,
        }
    }
}
</script>

<style lang="scss" scoped>
.right-div {
    flex-basis: 38%;
}
.button-card {
    padding: 35px;
    background: #1E1E1E;
    color: white;
    text-align: center;
    font-size: 17px;
    font-weight: 600;
}
</style>