<template>
    <ModalsOverlay>
        <div class="flex flex-col">
            <div class="flex items-start">
                <ModalsUpload />
                <ModalsFase view v-on="$listeners" :fase="fase" :data-konseling="dataJson" />
                <ModalsComment />
            </div>
            <div class="flex mt-5 justify-center">
                <button v-for="n in 8" @click="clickFase(n)" :class="{'active': n == active}" >Fase {{n}}</button>
            </div>
        </div>
    </ModalsOverlay>
</template>

<script>
export default {
    data(){
        return {
            fase: 1,
            active: 1,
            dataJson: {
                isi: "Lorem ipsum dolor sit amet, uctus massa placerat, euismod nunc. Sed eu enim sem. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nunc consectetur ac odio vitae pulvinar. Mauris ex eros, cursus non tellus sed, porttitor elementum lacus. Pellentesque ultrices lectus et gravida ornare.",
                perasaan: "Beberapa warga sedikit malu untuk masuk karena respon yang diterima kurang baik."
            }
        }
    },
    methods: {
        clickFase(val) {
            this.fase = val
            this.active = val
        }
    }
}
</script>

<style lang="scss" scoped>
button {
    box-shadow: 0px 0px 24px rgba(30, 30, 30, 0.1);
    border-radius: 10px;
    font-weight: 600;
    font-size: 19px;
    padding: 10px;
    margin: 0 11px;
    background-color: white;
    color: #1E1E1E;
}

button.active{
    background-color: #1E1E1E;
    color: white;
}
</style>