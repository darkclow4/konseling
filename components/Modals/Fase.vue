<template>
    <div class="card">
        <div class="flex items-start justify-between">
            <div class="flex flex-col mb-5 mr-5">
                <p class="card-title">Fase {{fase}}: {{textFase}}</p>
                <p class="label-font">Desa Margaasih Kabupaten Bandung</p>
                <p class="label-font">Home Visit</p>
                <p class="label-font">Selasa, 04 Oktober 2022 - 10:23</p>
                <p class="label-font">Desa Margaasih 19 Kab. Bandung 40002</p>
            </div>
            <img @click="closeModal" src="~/assets/img/icons/close.png" alt=""
                class="cursor-pointer aspect-square" width="30px">
        </div>

        <div class="input-container">
            <p class="label-font">Isi Interview</p>
            <textarea type="text" placeholder="Isi Interview di sini!" rows="8" :disabled="view">{{datajson.isi}}</textarea>
        </div>

        <div class="input-container">
            <p class="label-font">Perasaan Client</p>
            <textarea type="text" placeholder="Isi Perasaan Client di sini" rows="4" :disabled="view">{{datajson.perasaan}}</textarea>
        </div>

        <div v-show="!view" class="flex justify-end">
            <button class="btn mr-5 py-2" style="background-color: white; color: #1E1E1E" @click="$emit('draft')">Draft</button>
            <button class="btn py-2" @click="increment">{{nextButton}}</button>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            datajson: this.dataKonseling? this.dataKonseling: "",
        }
    },
    props: {
        fase: Number,
        dataKonseling: Object,
        view: {
            type: Boolean,
            default: false
        }
    },
    methods: {
        increment() {
            if(this.fase < 8) {
                this.$emit('increment')
            } else {
                this.$emit('finish')
            }
        },
        closeModal(){
            this.view ? this.$emit('close-modal') : this.$emit('draft')
        }
    },
    computed: {
        nextButton() {
            return this.fase == 8 ? "Selesai" : "Selanjutnya"
        },
        textFase () {
            switch(this.fase) {
                case 1:
                    return "Persiapan Awal"
                    break
                case 2:
                    return "Inisialisasi Sosial"
                    break
                case 3:
                    return "Asesmen Sosial"
                    break
                case 4:
                    return "Perencanaan Sosial"
                    break
                case 5:
                    return "Intervensi Sosial"
                    break
                case 6:
                    return "Peran Pekerja Sosial"
                    break
                case 7:
                    return "Moneva Sosial"
                    break
                case 8:
                    return "Terminasi & Rujukan"
                    break
                default:
                    return ""
                    break
            }
        }
    }
}
</script>

<style lang="scss" scoped>
textarea {
    width: 100%;
    background: rgba(30, 30, 30, 0.05);
    border-radius: 10px;
    font-weight: 500;
    font-size: 10px;
    color: #1E1E1E;
    padding: 8px 16px;

    &::placeholder {
        color: rgba(30, 30, 30, 0.3);
    }
}

.btn {
    text-align: center;
    font-weight: 500;
    font-size: 12px;
    background-color: #1E1E1E;
    color: white;
    border-radius: 10px;
    border: 1px solid rgba(30, 30, 30, 0.3);
    width: 35%;
}

.label-font {
    font-size: 12px;
    font-weight: 400;
    color: #1E1E1E;
}

.input-container {
    margin-bottom: 17px;

    p {
        margin-bottom: 6px;
    }
}
</style>