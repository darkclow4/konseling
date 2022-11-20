<template>
    <div class="sidebar-container flex flex-col shrink-0">
        <div class="flex-col">
            <div class="sidebar-title">
                <a href="/" class="text-white no-underline font-semibold">
                    {{sidebarList.title}}
                </a>
            </div>
            <hr>
        </div>
        <div class="flex flex-col justify-between grow mb-3 mt-4">
            <ul v-if="admin" class="flex-col mt-4">
                <li class="sidebar-li flex flex-row mb-3">
                    <NuxtLink to="/admin" class="w-full flex items-center py-3">
                        <img src="~/assets/img/icons/two people.svg" alt="" class="ml-5 mr-1">
                        <span class="link-text">Konselor</span>
                    </NuxtLink>
                </li>
                <li class="sidebar-li flex flex-row mb-3">
                    <NuxtLink to="/admin/supervisor" class="w-full flex items-center py-3">
                        <img src="~/assets/img/icons/many people.svg" alt="" class="ml-4">
                        <span class="link-text">Supervisor</span>
                    </NuxtLink>
                </li>
                <li class="sidebar-li flex flex-row mb-3">
                    <NuxtLink to="/admin/administrator" class="w-full flex items-center py-3">
                        <img src="~/assets/img/icons/admin.svg" alt="" class="ml-4">
                        <span class="link-text">Administrator</span>
                    </NuxtLink>
                </li>
            </ul>
            <ul v-else class="flex-col mt-4">
                <li class="sidebar-li flex flex-row mb-3">
                    <NuxtLink to="/home" class="w-full flex items-center py-3">
                        <img src="~/assets/img/icons/dashboard.png" alt="" class="ml-5 mr-1">
                        <span class="link-text">Dashboard</span>
                    </NuxtLink>
                </li>
                <li class="sidebar-li flex flex-row">
                    <NuxtLink to="/konseling" class="w-full flex items-center py-3">
                        <img src="~/assets/img/icons/analytics.png" alt="" class="ml-4">
                        <span class="link-text">Community Empowerment</span>
                    </NuxtLink>
                </li>
            </ul>
            <div class="user-container cursor-pointer" @click="toLogin">
                <div>
                    <img src="https://github.com/mdo.png" alt="" width="36" height="36" class="rounded-full">
                </div>

                <div class="flex justify-between flex-row w-full ml-2 items-center">
                    <div class="flex flex-col">
                        <p class="username font-medium">Mariansyah</p>
                        <p class="job font-normal">Konselor</p>
                    </div>

                    <img src="~/assets/img/icons/arrow_down.png" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            admin: false
        }
    },
    computed: {
        sidebarList(){
            if(this.$route.name.includes("admin")) {
                this.admin = true
                return {
                    title: "Manage User",
                    list: [
                        {
                            url: "~/assets/img/icons/two people.svg"
                        }
                    ]
                }
            } else {
                this.admin = false
                return {
                    title: "E-Community Empowerment"
                }
            }
        }
    },
    methods:{
        toLogin() {
            this.$router.push('/login')
        }
    }
}
</script>

<style lang="scss" scoped>
.sidebar-container {
    height: 100vh;
    width: 228px;
    background-color: #1E1E1E;
    padding: 25px 17px;
}

.sidebar-title {
    font-style: italic;
    font-size: 20px;
    text-align: center;
    width: 100%;
}

.sidebar-li {
    width: 100%;
    color: rgba(255, 255, 255, 0.3);
}

.link-text {
    margin-left: 4px;
    text-decoration: none;
    color: inherit;
    font-weight: 500;
    font-size: 15px;
}

.sidebar-li:hover {
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 10px;
    color: white;
}

.nuxt-link-exact-active {
    background-color: rgba(255, 255, 255, 0.05);
    border-radius: 10px;
    color: white;
}

.user-container {
    display: flex;
    background: #1E1E1E;
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 10px;
    padding: 6px 17px;
    align-items: center;
}

.username {
    font-size: 13px;
    margin: 0;
    padding: 0;
    color: white;
}

.job {
    font-size: 11px;
    margin: 0;
    padding: 0;
    color: rgba(255, 255, 255, 0.5);
}
</style>