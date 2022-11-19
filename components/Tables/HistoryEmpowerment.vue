<template>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th style="width: 28%;">Sasaran Perubahan</th>
                    <th style="width: 10%;">Waktu</th>
                    <th style="width: 28%;">Lokasi Sasaran Perubahan</th>
                    <th style="width: 25%;">Fasilitator</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Desa Margaasih Kabupaten Bandung</td>
                    <td>20 Okt 2022</td>
                    <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                    <td>Mariansyah, Hana Kana, Gilang, Irfan, Adi, Hari, Lia</td>
                    <td class="draft">Draft</td>
                </tr>
                <tr>
                    <td>Desa Margaasih Kabupaten Bandung</td>
                    <td>19 Okt 2022</td>
                    <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                    <td>Mariansyah, Hana Kana, Gilang</td>
                    <td class="finish">Selesai</td>
                </tr>
                <tr>
                    <td>Desa Margaasih Kabupaten Bandung</td>
                    <td>18 Okt 2022</td>
                    <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                    <td>Mariansyah, Hana Kana, Gilang</td>
                    <td class="finish">Selesai</td>
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

th, td {
    text-align: left;
    padding: 8px 10px;
    max-width: 0;
}

th {
    color: #D2D2D2;
    font-size: 9px;
    font-weight: 500;
}

td {
    color: #1E1E1E;
    font-size: 10px;
    font-weight: 600;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

tr {
    border-bottom: 1px solid #D2D2D2;
}

tbody tr:last-of-type {
    border-bottom: none;
}

.draft {
    color: #F8C43A;
}

.finish {
    color: #35D0BA;
}
</style>