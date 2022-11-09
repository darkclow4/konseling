<template>
    <div class="flex grow p-5 flex-col">
        <div class="flex mb-5 justify-end">
            <ButtonComponent 
                :url-image="require('~/assets/img/icons/delete.png')" 
                content="Delete Konseling"
                background="rgba(254, 95, 85, 0.3)"
            />
            <div class="flex ml-5 items-center search-container">
                <img src="~/assets/img/icons/search.png" alt="">
                <input type="text" placeholder="Search" class="ml-1 search-text">
            </div>
            <ButtonComponent 
                :url-image="require('~/assets/img/icons/add circle.png')" 
                content="Buat Konseling Makro Baru!"
                background="#1E1E1E"
            />
        </div>
        <div class="flex-auto table-container">
            <TableComponent />
        </div>
    </div>
</template>

<script>
    export default {
        layout: "dashboard",
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
    color: rgba(30, 30, 30, 0.5);
    width: 100%;

    &:focus{
        outline: none;
    };
}
</style>