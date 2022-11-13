<template>
    <ModalsOverlay>
        <ModalsDraft v-if="draft" v-on="$listeners" @close-modal="resetFase" 
            :url-image="require('~/assets/img/draft.png')"
            title="Konseling Disimpan di Draft!"
            subtitle="Konseling ini disimpan sementara di bagian Draft."
        />
        <ModalsDraft v-else-if="finish" v-on="$listeners" @close-modal="resetFase" 
            :url-image="require('~/assets/img/verified.png')"
            title="Konseling Sudah Selesai"
            subtitle="Seluruh fase dalam konseling ini sudah selesai."
        />
        <div v-else class="flex items-start">
            <ModalsUpload />
            <div class="flex flex-col">
                <ModalsFase v-on="$listeners" :fase=dataFase @increment="increment" @finish="showFinish" @draft="showDraft" />
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
            draft: false,
            finish: false
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
        },
        showFinish() {
            this.finish = true
        },
        resetFase() {
            this.dataFase = 1
            this.draft=false
            this.finish=false
        },
        showDraft(){
            this.draft = true
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