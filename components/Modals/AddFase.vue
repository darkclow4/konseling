<template>
    <ModalsOverlay>
        <div class="flex items-start">
            <ModalsUpload />
            <div class="flex flex-col">
                <ModalsFase v-on="$listeners" :fase=dataFase @increment="increment" @finish="finish" />
                <button v-show="showBack" class="back-btn py-3 mt-5" @click="decrement">Kembali ke Fase {{textFase}}</button>
            </div>
        </div>
    </ModalsOverlay>
</template>

<script>
export default {
    data(){
        return {
            dataFase: this.fase,
        }
    },
    props: {
        fase: {
            type: Number,
            default: 1
        },
    },
    methods: {
        increment() {
            this.dataFase++
        },
        decrement() {
            this.dataFase--
            console.log(this.dataFase)
        },
        finish() {
            this.dataFase = 1
        }
    },
    computed: {
        textFase() {
            return this.dataFase-1
        },
        showBack() {
            return this.dataFase>1
        }
    }
}
</script>

<style lang="scss" scoped>
.back-btn {
    background-color: #1E1E1E;
    color: white;
    font-size: 20px;
    font-weight: 500;
    text-align: center;
    border-radius: 10px;
}
</style>