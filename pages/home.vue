<template>
    <div class="flex grow p-5">
        <div class="flex flex-col flex-auto">
            <div class="flex basis-1/3">
                <div @click="showModal = true"
                    class="flex flex-col justify-center items-center cursor-pointer card button-card aspect-square mr-5 shrink-0">
                    <img src="~/assets/img/icons/plus.png" alt="" width="40%">
                    <p class="my-4 2xl:text-xl">Buat Community Empowerment Baru</p>
                </div>
                <div class="flex card flex-col grow justify-between">
                    <div class="flex flex-col">
                        <p class="card-title mb-3">Riwayat Community Empowerment</p>
                        <TablesHistoryEmpowerment />
                    </div>

                    <div class="flex justify-end mt-3">
                        <PaginationNumber content="1" active />
                        <PaginationNumber content="2" />
                        <PaginationNumber content="3" />
                        <PaginationNumber content="4" />
                        <PaginationNumber content="5" />
                    </div>
                </div>
            </div>
            <div class="flex basis-2/3 card mt-5 flex-col justify-between">
                <div class="flex flex-col">
                    <div class="flex justify-between items-center mb-5">
                        <p class="card-title">Quick Access Community Empowerment</p>
                        <div class="flex ml-5 items-center search-container">
                            <img src="~/assets/img/icons/search.png" alt="" width="18px" class="mx-1">
                            <input type="text" placeholder="Cari Sasaran Perubahan" class="ml-1 search-text">
                        </div>
                    </div>
                    <TablesQuickEmpowerment />
                </div>

                <div class="flex justify-end mt-3">
                    <PaginationNumber content="1" active />
                    <PaginationNumber content="2" />
                    <PaginationNumber content="3" />
                    <PaginationNumber content="4" />
                    <PaginationNumber content="5" />
                </div>
            </div>
        </div>
        <div v-if="konseling" class="flex flex-col card ml-5 right-div">
            <p class="card-title">Jadwal Konseling Terdekat</p>
            <NearlyKonseling />
            <NearlyKonseling />
            <NearlyKonseling />
            <NearlyKonseling />
        </div>
        <ModalsNewEmpowerment v-show="showModal" @close-modal="showModal = false" @next-modal="showNextModal" />
        <ModalsAddFase v-show="nextModal" @close-modal="nextModal = false" />
    </div>
</template>

<script>
export default {
    layout: "dashboard",
    data() {
        return {
            showModal: false,
            nextModal: false,
            konseling: false
        }
    },
    methods: {
        showNextModal() {
            this.showModal = false
            this.nextModal = true
        }
    }
}
</script>

<style lang="scss" scoped>
.right-div {
    flex-basis: 42%;
}

.button-card {
    width: 21%;
    padding: 20px;
    background: #1E1E1E;
    color: white;
    text-align: center;
    font-size: 17px;
    font-weight: 600;
}

.search-container {
    padding: 8px;
    background-color: white;
    border-radius: 10px;
    border: 1px solid #D2D2D2;
    width: 30%;
}

.search-text {
    font-weight: 500;
    font-size: 12px;
    color: #1E1E1E;
    width: 100%;

    &:focus {
        outline: none;
    }

    ;

    &::placeholder {
        color: rgba(30, 30, 30, 0.5);
    }
}
</style>