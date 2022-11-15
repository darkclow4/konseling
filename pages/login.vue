<template>
  <div>
    <div class="signin-container text-center">
        <p class="font-semibold mb-3" style="font-size: 23px;">Login Disini!</p>
        <p class="mx-auto font-medium mb-8" style="font-size: 14px; color: rgba(30, 30, 30, 0.3); width: 246px;">
            Silahkan login menggunakan akun E-Konseling anda!
        </p>
        <form>
            <p v-show="error" class="error">{{errorMsg}}</p>
            <input type="email" class="form-input" placeholder="Username" v-model="username" required>
            <input type="password" class="form-input" placeholder="Password" v-model="password" required>
            <button type="submit" class="form-btn" @click.prevent="authLogin">Login</button>
        </form>
        <p class="font-medium mb-3" style="font-size: 11px; color: rgba(30, 30, 30, 0.3);">Belum punya akun?</p>
        <button class="btn-contact">
            Kontak Administrasi!
        </button>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'login_bg',
  data(){
    return{
        username: "",
        password: "",
        error: false,
        errorMsg: ""
    }
  },
  methods: {
    toRole() {
        this.$router.push('/role')
    },
    authLogin () {
        const user = JSON.parse(localStorage.getItem("data")).user[0]
        if(user.username == this.username && user.password == this.password){
            this.toRole()
        } else {
            this.error = true
            this.errorMsg = this.username == user.username ? "Password tidak sesuai" : "Username salah"
        }
    }
  }
}
</script>

<style lang="scss">
$mediumFont: 14px;

.signin-container {
    width: 300px;
    background-color: white;
    box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.25);
    border-radius: 10px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 2;
    padding: 45px 22px;
}

.form-input {
    margin-bottom: 17px;
    padding: 8px 17px;
    border-radius: 10px;
    font-size: $mediumFont;
    font-weight: 500;
    background: rgba(30, 30, 30, 0.05);
    width: 100%;
}

.form-btn {
    background: #1E1E1E;
    border-radius: 10px;
    color: #FFFFFF;
    font-weight: 600;
    font-size: $mediumFont;
    width: 100%;
    margin-bottom: 34px;
    padding: 8px;
}

.form-btn:hover {
    background-color: rgba(30, 30, 30, 0.5);
}

.btn-contact {
    background: #FFFFFF;
    border: 1px solid rgba(30, 30, 30, 0.2);
    border-radius: 10px;
    font-weight: 600;
    font-size: $mediumFont;
    color: #1E1E1E;
    width: 100%;
    padding: 8px;
}

.btn-contact:hover {
    background-color: rgba(30, 30, 30, 0.5);
}

.error {
    font-size: $mediumFont;
    font-weight: 500;
    background-color: rgb(216, 44, 44);
    color: white;
    border-radius: 10px;
    padding: 5px;
    margin-bottom: 15px;
}
</style>