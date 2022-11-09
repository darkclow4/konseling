<template>
    <table>
        <tr>
            <th>Konselor</th>
            <th>Client</th>
            <th>Waktu Wawancara</th>
            <th>Lokasi Konseling</th>
            <th>Jenis Lokasi</th>
            <th>Fase Selesai</th>
            <th>Status Konseling</th>
        </tr>
        <tr>
            <td>Beberapa konselor</td>
            <td>Desa Margaasih Bandung</td>
            <td>Minggu, 30 Okt 2022 10:00</td>
            <td>Desa Margaasih 19 Kab. Bandung 40002</td>
            <td>
                <HomeVisit />
            </td>
            <td>Fase 1 fase 2</td>
            <td>Selesai</td>
        </tr>
        <tr>
            <td>Beberapa konselor</td>
            <td>Desa Margaasih Bandung</td>
            <td>Minggu, 30 Okt 2022 10:00</td>
            <td>Desa Margaasih 19 Kab. Bandung 40002</td>
            <td>
                <HomeVisit />
            </td>
            <td>Fase 1 fase 2</td>
            <td>Selesai</td>
        </tr>
    </table>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
table {
    width: 100%;
}
th {
    height: 20px;
    border-top: 1px solid black;
}
tr {
    border: {
        bottom: 1px solid black;
    }
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
</style>