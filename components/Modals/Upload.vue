<template>
    <div class="flex flex-col mr-5 card w-2/5">
        <p class="card-title">Upload File</p>
        <p class="normal-text font-normal">Tambah File atau Link Cloud di sini!</p>
        <div class="my-5 p-5 items-center justify-center flex flex-col upload-container cursor-pointer">
            <img src="~/assets/img/icons/upload.png" alt="" width="30%">
            <p class="upload-font mt-3 px-8">Tekan di sini atau Tarik File ke sini!</p>
        </div>
        <p class="normal-text font-normal">Atau Simpan Link di bawah!</p>
        <input type="text" placeholder="Link GDrive, Dropbox, dll.">
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.upload-font {
    font-weight: 600;
    font-size: 13px;
    color: rgba(30, 30, 30, 0.2);
    text-align: center;
}
.upload-container {
    border: 2px dashed rgba(30, 30, 30, 0.2);
    border-radius: 10px;
}
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
</style>