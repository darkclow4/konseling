<template>
    <div class="flex grow">
        <div class="flex grow p-5 flex-col">
            <div class="flex mb-5 justify-end">
                <ButtonComponent :url-image="require('~/assets/img/icons/delete.png')" content="Delete"
                    background="rgba(254, 95, 85, 0.3)" />
                <div class="flex ml-5 items-center search-container">
                    <img src="~/assets/img/icons/search.png" alt="">
                    <input type="text" placeholder="Cari Client" class="ml-1 search-text">
                </div>
            </div>
            <div class="flex-auto table-container">
                <TablesEmpowerment @click="viewModal = true" />
            </div>
        </div>
        <ModalsViewFase v-show="viewModal" @close-modal="viewModal = false" />
    </div>
</template>

<script>
export default {
    layout: "dashboard",
    data() {
        return {
            viewModal: false
        }
    },
    methods: {
    }
}
</script>

<style lang="scss" scoped>
.table-container {
    background-color: white;
    box-shadow: 0px 0px 24px rgba(30, 30, 30, 0.1);
    border-radius: 10px;
}

.search-container {
    padding: 10px;
    background-color: white;
    box-shadow: 0px 0px 24px rgba(30, 30, 30, 0.1);
    border-radius: 10px;
    width: 300px;
}

.search-text {
    font-weight: 500;
    font-size: 12px;
    color: #1E1E1E;
    width: 100%;

    &:focus {
        outline: none;
    };

    &::placeholder {
        color: rgba(30, 30, 30, 0.5);
    }
}
</style>