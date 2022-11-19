<template>
  <div class="flex w-screen h-screen justify-center items-center">
    <div class="card">
      <p>E-Konseling Landing Page</p>
    </div>
    <NuxtLink to="/login">
      <div class="card absolute top-10 right-10">
        Login
      </div>
    </NuxtLink>
  </div>
</template>

<script>

export default {
  layout: "login_bg",
  mounted() {
    const datajson = {
      user: [
          {
            id: 1,
            username: "testing",
            password: "testing",
            role: "mahasiswa"
          },
          {
            id: 2,
            username: "supervisor",
            password: "supervisor",
            role: "supervisor",
          },
          {
            id: 3,
            username: "admin",
            password: "admin",
            role: "admin"
          }
        ]
    }
    const dataStorage = JSON.parse(localStorage.getItem("datakonseling"))
    
    if(dataStorage){
      console.log(dataStorage.user[0].username)
    } else {
      localStorage.setItem("datakonseling", JSON.stringify(datajson))
    }
  }
}
</script>

<style lang="scss" scoped>

</style>