<template>
    <div class="flex header-container py-6 px-14">
        <p class="font-semibold text-3xl italic">{{title}}</p>
    </div>
</template>

<script>
    export default {
        computed: {
            title(){
                const routeName = this.$route.name
                if(routeName.includes("admin")){
                    if(routeName.includes("supervisor")){
                        return "Supervisor"
                    } else if (routeName.includes("administrator")) {
                        return "Administrator"
                    } else {
                        return "Konselor"
                    }
                }
                return routeName === "home" ? "Dashboard" : "Community Empowerment";
            }
        }
    }
</script>

<style lang="scss" scoped>
.header-container {
    background: white;
    height: 80px;
}
</style>