<template>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th style="width: 22%;">Fasilitator</th>
                    <th style="width: 15%;">Sasaran Perubahan</th>
                    <th style="width: 8%;">Waktu</th>
                    <th>Lokasi Sasaran Perubahan</th>
                    <th style="width: 25%;">Fase Selesai</th>
                    <th style="width: 5%;">Aksi</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>
                        <ButtonView content="Mariansyah" />
                        <ButtonView content="Hana" />
                        <ButtonView content="Kana" />
                        <ButtonView content="Hari" />
                        <ButtonView content="Gilang" />
                        <ButtonView content="Rendi" />
                    </td>
                    <td>Desa Margaasih Kabupaten Bandung</td>
                    <td>20 Okt 2022 10:00</td>
                    <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                    <td>
                        <ButtonView content="Fase1" />
                        <ButtonView content="Fase2" />
                        <ButtonView content="Fase3" />
                        <ButtonView content="Fase4" />
                        <ButtonView content="Fase5" />
                        <ButtonView content="Fase6" />
                        <ButtonView content="Fase7" />
                    </td>
                    <td>
                        <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                    </td>
                </tr>
                <tr>
                    <td>
                        <ButtonView content="Helmi Ilham Fauzi" />
                        <ButtonView content="Hamzah Fatah" />
                        <ButtonView content="Rahmat Mandala" />
                        <ButtonView content="Ghaza Supratna" />
                    </td>
                    <td>Desa Margaasih Kabupaten Bandung</td>
                    <td>20 Okt 2022 10:00</td>
                    <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                    <td>
                        <ButtonView content="Fase1" />
                        <ButtonView content="Fase2" />
                        <ButtonView content="Fase3" />
                        <ButtonView content="Fase4" />
                        <ButtonView content="Fase5" />
                        <ButtonView content="Fase6" />
                        <ButtonView content="Fase7" />
                    </td>
                    <td>
                        <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.table-container {
    border: 1px solid #D2D2D2;
    border-radius: 5px;
}

table {
    width: 100%;
}

th,
td {
    padding: 10px 10px;
    text-align: left;
    vertical-align: top;
    color: #1E1E1E;
}

th {
    font-weight: 600;
    font-size: 12px;
}

td {
    font-weight: 500;
    font-size: 11px;
}

tr {
    border-bottom: 1px solid #D2D2D2;
}

tbody tr:last-of-type {
    border-bottom: none;
}

.delete-btn {
    background-color: rgba(255, 52, 52, 0.9);
    border-radius: 5px;
    padding: 4px;
}
</style>