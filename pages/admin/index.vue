<template>
    <div class="flex grow flex-col p-5">
        <div class="flex mb-5 justify-end">
            <div class="flex ml-5 items-center search-container">
                <img src="~/assets/img/icons/search.png" alt="" width="20px">
                <input type="text" placeholder="Cari Konselor" class="ml-1 search-text">
            </div>
            <ButtonComponent :url-image="require('~/assets/img/icons/import.svg')" content="Ekspor Data"
                background="#EE712B" />
            <ButtonComponent :url-image="require('~/assets/img/icons/import.svg')" content="Impor Data"
                background="#35D0BA" />
            <ButtonComponent :url-image="require('~/assets/img/icons/add.svg')" content="Tambah Konselor"
                background="#0C9CEE" @click="addModal = true" />
        </div>
        <div class="table-container grow">
            <TablesAdminKonselor @click-edit="editModal = true" />
        </div>
        <ModalsAdminAdd v-show="addModal" @close-modal="addModal = false" />
        <ModalsAdminEdit v-show="editModal" @close-modal="editModal = false" />
    </div>
</template>

<script>
export default {
    layout: "dashboard",
    data(){
        return{
            addModal:false,
            editModal: false
        }
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
    }

    ;

    &::placeholder {
        color: rgba(30, 30, 30, 0.5);
    }
}
</style>