<template>
    <div class="box-container flex justify-center">
        <div class="role-container p-5">
            <div class="flex items-center cursor-pointer" @click="toLogin">
                <img src="~/assets/img/icons/arrow back.png" alt="back" width="20px">
                <p class="ml-3 normal-text">Kembali</p>
            </div>
            <p class="text-xl font-semibold mt-3" style="color: #1E1E1E">Pilih {{ title }}!</p>
            <p class="normal-text mt-3 mb-5" style="color: rgba(30, 30, 30, 0.3);">Pilih {{ subtitle }} yang tersedia di
                bawah.</p>
            <div v-show="!konseling" class="flex">
                <RoleCard class="mr-5" @click.native="konseling = true" :img-url="require('~/assets/img/konseling.png')"
                    content="Konseling adalah kegiatan untuk melakukan interview dengan seorang client."
                    footer="Konseling" />
                <RoleCard @click.native="toHome" :img-url="require('~/assets/img/empowerment.png')"
                    content="E-Community Empowerment adalah konseling yang melibatkan banyak grup dan banyak orang."
                    footer="E-Community Empowerment" />
            </div>
            <div v-show="konseling" class="flex">
                <RoleCard class="mr-5" :img-url="require('~/assets/img/konselor.png')" content="Konselor adalah"
                    footer="Konselor" />
                <RoleCard :img-url="require('~/assets/img/client.png')" content="Client adalah" footer="Client" />
            </div>
        </div>

        <div v-if="!konseling" class="admin-container p-5 flex flex-col justify-between">
            <div>
                <p class="text-xl font-semibold mt-3" style="color: #1E1E1E">Manajemen User</p>
                <p class="normal-text mt-3 mb-5" style="color: rgba(30, 30, 30, 0.3);">Mengatur data pengguna.</p>
            </div>
            <RoleCard @click.native="toAdmin" :img-url="require('~/assets/img/admin.png')"
                content="Manajemen User adalah mode untuk Administrasi melakukan perubahan, tambah, dan hapus data pengguna."
                footer="Manajemen User" />
        </div>
    </div>
</template>

<script>
export default {
    layout: 'login_bg',
    data() {
        return {
            konseling: false,
        }
    },
    methods: {
        toLogin() {
            if (this.konseling) {
                this.konseling = false
            } else {
                this.$router.push('/login')
            }
        },
        toHome() {
            this.$router.push('/home')
        },
        toAdmin(){
            this.$router.push('/admin')
        }
    },
    computed: {
        title() {
            return this.konseling ? "Role yang diinginkan" : "Jenis Konseling"
        },
        subtitle() {
            return this.konseling ? "dua role" : "dua jenis konseling"
        }
    }
}
</script>

<style lang="scss" scoped>
.box-container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    // background: #FFFFFF;
    width: 100%;
    // box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.25);
    // border-radius: 10px;
    // width: 33%;
}

.role-container {
    background-color: #FFFFFF;
    box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.25);
    border-radius: 10px;
    width: 33%;
}

.admin-container {
    background-color: white;
    box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.25);
    border-radius: 10px;
    margin-left: 22px;
    width: 230px;
}

.normal-text {
    font-size: 12px;
    color: #1E1E1E;
    font-weight: 500;
}
</style>