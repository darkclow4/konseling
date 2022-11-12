<template>
    <div>
        <table class="roundedCorners">
            <tr>
                <th>Client</th>
                <th>Lokasi Konseling</th>
                <th>Waktu</th>
                <th style="width: 15%;">Konseling</th>
                <th>Aksi</th>
            </tr>
            <tr>
                <td>Desa Margaasih Kabupaten Bandung</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                <td>20 Oktober 2022 10:00</td>
                <td><ButtonView content="Home Visit" /></td>
                <td>
                    <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                </td>
            </tr>
            <tr>
                <td>Desa Margaasih Kabupaten Bandung</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                <td>20 Oktober 2022 10:00</td>
                <td><ButtonView content="Home Visit" /></td>
                <td>
                    <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                </td>
            </tr>
            <tr>
                <td>Desa Margaasih Kabupaten Bandung</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                <td>20 Oktober 2022 10:00</td>
                <td><ButtonView content="Home Visit" /></td>
                <td>
                    <button class="delete-btn"><img src="~/assets/img/icons/delete.png" width="18px"></button>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
table {
    border-spacing: 0;
    border: 1px solid #D2D2D2;
}
tr {
    border-bottom: 1px solid #D2D2D2;
}

tr td:first-child, tr th:first-child {
    padding-left: 20px;
}

tr td:last-child, tr th:last-child {
    padding-right: 20px;
}

th,
td {
    padding: 10px 5px;
    text-align: left;
    vertical-align: top;
}

th {
    font-weight: 500;
    font-size: 11px;
}

td {
    font-weight: 400;
    font-size: 11px;
}

th:first-of-type {
    border-top-left-radius: 10px;
}

th:last-of-type {
    border-top-right-radius: 10px;
}

tr:last-of-type td:first-of-type {
    border-bottom-left-radius: 10px;
}

tr:last-of-type td:last-of-type {
    border-bottom-right-radius: 10px;
}

.delete-btn {
    background-color: rgba(255, 52, 52, 0.9);
    border-radius: 5px;
    padding: 4px;
}
</style>