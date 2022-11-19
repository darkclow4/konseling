<template>
    <ModalsOverlay>
        <div class="card" style="width: 340px;">
            <div class="flex items-start justify-between">
                <div class="flex flex-col mb-5">
                    <p class="card-title">Buat Empowerment Baru</p>
                    <p class="label-font">Selasa, 04 Oktober 2022 - 10:23</p>
                </div>
                <img @click="$emit('close-modal')" src="~/assets/img/icons/close.png" alt="" class="cursor-pointer aspect-square" width="30px">
            </div>

            <div class="input-container">
                <p class="label-font">Sasaran Perubahan <span class="red-text">*</span></p>
                <input type="text" placeholder="Isi Sasaran Perubahan">
            </div>

            <div class="input-container">
                <p class="label-font">Nama Fasilitator <span class="red-text">*</span> 
                    <span class="italic" style="font-size: 9px; color: rgba(30, 30, 30, 0.3);">
                        (Maksimal 15 orang)
                    </span>
                </p>
                <input type="text" placeholder="Isi Nama Fasilitator">
            </div>

            <div class="input-container">
                <p class="label-font">Lokasi Sasaran Perubahan <span class="red-text">*</span></p>
                <textarea type="text" placeholder="Isi Lokasi Sasaran Perubahan" rows="3"></textarea>
                <p class="label-font mt-1.5 red-text italic">* Wajib diisi</p>
            </div>

            <button @click="$emit('next-modal')" class="btn mx-auto">Buat Konseling</button>
        </div>
    </ModalsOverlay>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.label-font {
    font-size: 12px;
    font-weight: 400;
    color: #1E1E1E;
}

input, select, textarea {
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

.input-container {
    margin-bottom: 17px;

    p {
        margin-bottom: 6px;
    }
}

.btn {
    display: block;
    background-color: #1E1E1E;
    color: white;
    width: 50%;
    padding: 9px;
    border-radius: 10px;
    font: {
        size: 12px;
        weight: 500;
    }
}

.red-text {
    color: #FE5F55;
}
</style>