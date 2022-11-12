<template>
    <div>
        <table class="width: 100%">
            <tr>
                <th style="width: 25%;">Client</th>
                <th style="width: 19%;">Waktu</th>
                <th>Alamat client</th>
                <th style="width: 23%;">Tipe Konseling</th>
            </tr>
            <tr>
                <td>Desa Margaas..</td>
                <td>20 Okt 2022</td>
                <td>Desa Margaasih Kab..</td>
                <td>Home Visit</td>
            </tr>
            <tr>
                <td>Desa Margaas..</td>
                <td>20 Okt 2022</td>
                <td>Desa Margaasih Kab..</td>
                <td>Home Visit</td>
            </tr>
            <tr>
                <td>Desa Margaas..</td>
                <td>20 Okt 2022</td>
                <td>Desa Margaasih Kab..</td>
                <td>Home Visit</td>
            </tr>
        </table>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
tr {
    border-bottom: 1px solid #D2D2D2;
    border-right: 1px solid #D2D2D2;
    border-left: 1px solid #D2D2D2;
}

th, td {
    text-align: left;
    padding: 6px;
    vertical-align: top;
}

th {
   color: #D2D2D2;
   font-size: 9px;
   font-weight: 500;
   border-top: 1px solid #D2D2D2;
}

td {
    color: #1E1E1E;
    font-size: 10px;
    font-weight: 600;
}
</style>