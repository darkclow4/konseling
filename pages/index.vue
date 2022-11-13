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
  layout: "login_bg"
}
</script>

<style lang="scss" scoped>

</style>