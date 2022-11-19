<template>
    <div class="relative px-5">
        <div class="header-background absolute top-0 left-0 right-0"></div>
        <table class="relative">
            <tr>
                <th>Fasilitator</th>
                <th style="width: 18%">Sasaran Perubahan</th>
                <th style="width: 15%">Waktu Wawancara</th>
                <th style="width: 17%">Lokasi</th>
                <th style="width: 15%;">Fase Selesai</th>
                <th style="width: 10%">Status</th>
            </tr>
            <tr @click="$emit('click')">
                <td>
                    <ButtonView content="Helmi Ilham Fauzi" />
                    <ButtonView content="Hamzah Fatah" />
                    <ButtonView content="Rahmat Mandala" />
                    <ButtonView content="Ghaza Supratna" />
                </td>
                <td>Desa Margaasih Bandung</td>
                <td>Minggu, 30 Okt 2022 10:00</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
                <td>
                    <ButtonView content="Fase1" />
                    <ButtonView content="Fase2" />
                    <ButtonView content="Fase3" />
                    <ButtonView content="Fase4" />
                    <ButtonView content="Fase5" />
                    <ButtonView content="Fase6" />
                    <ButtonView content="Fase7" />
                    <ButtonView content="Fase8" />
                </td>
                <td>
                    <ButtonView content="Selesai" />
                </td>
            </tr>
            <tr>
                <td>
                    <ButtonView content="Helmi Ilham Fauzi" />
                    <ButtonView content="Hamzah Fatah" />
                    <ButtonView content="Rahmat Mandala" />
                    <ButtonView content="Ghaza Supratna" />
                </td>
                <td>Desa Margaasih Bandung</td>
                <td>Minggu, 30 Okt 2022 10:00</td>
                <td>Desa Margaasih 19 Kab. Bandung 40002</td>
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

tr td {
    cursor: pointer;
}
</style>