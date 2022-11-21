<template>
    <div class="relative px-5">
        <div class="header-background absolute top-0 left-0 right-0"></div>
        <table class="relative">
            <thead>
                <tr>
                    <th>Nama {{name}}</th>
                    <th style="width: 18%">No. Identitas</th>
                    <th style="width: 15%">Jenis Kelamin</th>
                    <th style="width: 17%">Hak Akses</th>
                    <th style="width: 15%;">Masa Berlaku</th>
                    <th style="width: 10%">Aksi</th>
                </tr>
            </thead>
            <tbody>
                <tr @click="$emit('click')">
                    <td>Mariansyah</td>
                    <td>123456789012345</td>
                    <td>Laki-laki</td>
                    <td>
                        <ButtonView content="E Konseling" />
                        <ButtonView content="E Community Empowerment" />
                    </td>
                    <td>12 Desember 2023</td>
                    <td>
                        <button class="edit-btn" @click="$emit('click-edit')"><img src="~/assets/img/icons/edit.svg" width="18px"></button>
                        <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                    </td>
                </tr>
                <tr>
                    <td>Hana Kana</td>
                    <td>123456789012345</td>
                    <td>Perempuan</td>
                    <td>
                        <ButtonView content="E Konseling" />
                    </td>
                    <td>12 Desember 2023</td>
                    <td>
                        <button class="edit-btn" @click="$emit('click-edit')"><img src="~/assets/img/icons/edit.svg" width="18px"></button>
                        <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    computed: {
        name(){
            if(this.$route.name.includes("supervisor")){
                return "Supervisor"
            } else {
                return "Konselor"
            }
        }
    }
}
</script>

<style lang="scss" scoped>
$primary_color: #1E1E1E;

.header-background {
    background-color: #1E1E1E;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    height: 40px;
}

table {
    width: 100%;
    z-index: 1;
}

th,
td {
    padding-top: 10px;
    padding-bottom: 10px;
}

th {
    font-size: 12px;
    font-weight: 500;
    height: 40px;
    color: white;
    text-align: left;
}

td {
    font-size: 12px;
    font-weight: 400;
    color: $primary_color;
    border-bottom: 1px solid rgb(30, 30, 30, 0.3);
    vertical-align: top;
    padding-right: 10px;
}

tr td {
    cursor: pointer;
}

.delete-btn {
    background-color: #FE5F55;
    border-radius: 5px;
    padding: 4px;
}

.edit-btn {
    background-color: #35D0BA;
    border-radius: 5px;
    padding: 4px;
    margin-right: 8px;
}
</style>