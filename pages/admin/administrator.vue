<template>
    <div class="flex grow flex-col p-5">
        <div class="flex mb-5 justify-end">
            <div class="flex ml-5 items-center search-container">
                <img src="~/assets/img/icons/search.png" alt="" width="20px">
                <input type="text" placeholder="Cari Admin" class="ml-1 search-text">
            </div>
            <ButtonComponent :url-image="require('~/assets/img/icons/add.svg')" content="Tambah Admin"
                background="#0C9CEE" />
        </div>
        <div class="table-container grow">
            <TablesAdminAdministrator />
        </div>
    </div>
</template>

<script>
    export default {
        layout: "dashboard"
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