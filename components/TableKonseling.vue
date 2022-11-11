<template>
    <div class="relative px-5">
        <div class="header-background absolute top-0 left-0 right-0"></div>
        <table class="relative">
            <tr>
                <th>Konselor</th>
                <th style="width: 13%">Client</th>
                <th style="width: 15%">Waktu Wawancara</th>
                <th style="width: 12%">Lokasi Konseling</th>
                <th style="width: 10%">Jenis Lokasi</th>
                <th style="width: 15%;">Fase Selesai</th>
                <th style="width: 13%">Status Konseling</th>
            </tr>
            <tr>
                <td>
                    <p>Mariansyah</p>
                    <p>Gilang</p>
                </td>
                <td>Desa Margaasih Bandung</td>
                <td>Minggu, 30 Okt 2022 10:00</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                <td>
                    <ButtonView content="Home Visit" />
                </td>
                <td>
                    <ButtonView content="Fase1" />
                    <ButtonView content="Fase2" />
                    <ButtonView content="Fase3" />
                    <ButtonView content="Fase4" />
                </td>
                <td>
                    <ButtonView content="Selesai" />
                </td>
            </tr>
            <tr>
                <td>Mariansyah</td>
                <td>Desa Margaasih Bandung</td>
                <td>Minggu, 30 Okt 2022 10:00</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                <td>
                    <ButtonView content="Home Visit" />
                </td>
                <td>
                    <ButtonView content="Fase1" />
                    <ButtonView content="Fase2" />
                </td>
                <td>
                    <ButtonView content="Draft" />
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