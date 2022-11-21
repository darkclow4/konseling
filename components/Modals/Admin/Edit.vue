<template>
    <ModalsOverlay>
        <div class="card">
            <div class="flex items-start justify-between mb-3">
                <p class="card-title mr-6">Ubah Data Konselor</p>
                <img @click="$emit('close-modal')" src="~/assets/img/icons/close.png" alt=""
                    class="cursor-pointer aspect-square" width="30px">
            </div>

            <div class="input-container">
                <p class="label-font">Nama Konselor <span class="red-text">*</span></p>
                <input type="text" placeholder="Isi Nama Konselor" value="Mariansyah">
            </div>

            <div class="input-container">
                <p class="label-font">Nomor Identitas <span class="red-text">*</span></p>
                <input type="text" placeholder="Isi Nomor Identitas" value="123456789012345">
            </div>

            <div class="input-container">
                <p class="label-font">Jenis Kelamin <span class="red-text">*</span></p>
                <select name="" id="" required>
                    <option value="" disabled selected hidden>Pilih Jenis Kelamin</option>
                    <option value="0" selected>Laki-laki</option>
                    <option value="1">Perempuan</option>
                </select>
            </div>

            <div class="input-container">
                <p class="label-font">Masa Berlaku <span class="red-text">*</span></p>
                <input type="date" placeholder="Tentukan Masa Berlaku" value="2023-12-14">
            </div>

            <div class="input-container">
                <p class="label-font">Username <span class="red-text">*</span></p>
                <input type="text" placeholder="Isi Username" value="mariansyah123">
            </div>

            <div class="input-container">
                <p class="label-font">Password <span class="red-text">*</span></p>
                <input type="password" placeholder="Isi Password" value="asdfasdf">
            </div>

            <div class="input-container">
                <p class="label-font">Hak Akses <span class="red-text">*</span> <span class="italic"
                        style="font-size: 9px; color: rgba(30, 30, 30, 0.5);">
                        (Dapat dipilih 2 Hak Akses)
                    </span></p>
                <div class="flex justify-start">
                    <input type="checkbox" style="width: 18px; margin-right: 7px;" checked>
                    <ButtonView content="E Konseling" />
                </div>
                <div class="flex justify-start">
                    <input type="checkbox" style="width: 18px; margin-right: 7px;" checked>
                    <ButtonView content="E Community Empowerment" />
                </div>
                <p class="label-font mt-1.5 red-text italic">* Wajib diisi</p>
            </div>

            <button class="mx-auto block">Ubah Konselor</button>
        </div>
    </ModalsOverlay>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
select:invalid {
    color: rgba(30, 30, 30, 0.3);
}

option {
    color: #1E1E1E;
}

.label-font {
    font-size: 12px;
    font-weight: 400;
    color: #1E1E1E;
}

input,
select {
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
    margin-bottom: 12px;

    p {
        margin-bottom: 6px;
    }
}

p.red-text {
    font-size: 9px;
}

.red-text {
    color: #FE5F55;
}

button {
    font-weight: 600;
    font-size: 11px;
    background-color: #1E1E1E;
    padding: 8px;
    color: white;
    text-align: center;
    border-radius: 10px;
    width: 180px;
}
</style>