<template>
    <div class="inline-flex m-px">
        <div class="flex items-center container-card w-fit p-1" :style="{ backgroundColor: background }">
            <p class="container-text">{{ content }}</p>
            <img v-if="showImg" src="~/assets/img/icons/check.png" width="30%" class="ml-1" />
        </div>
    </div>
</template>

<script>
export default {
    props: {
        content: String
    },
    computed: {
        background() {
            if (this.content.includes("Fase")) {
                return "#492B7B"
            } else if (this.content.includes("E Konseling") || this.content.includes("E Community")) {
                return "#0C9CEE"
            }
            switch (this.content) {
                case "Home Visit":
                    return "#0C9CEE"
                    break;
                case "Selesai":
                    return "#35D0BA"
                    break;
                case "Draft":
                    return "#F8C43A"
                    break;
                case "Admin":
                    return "#EE712B"
                    break;
                default:
                    return "#1E1E1E"
                    break;
            }
        },
        showImg() {
            if (this.content.includes("Fase")) {
                return true;
            } else {
                return false;
            }
        }
    }
}
</script>

<style lang="scss" scoped>
.container-card {
    border-radius: 5px;
}

.container-text {
    color: white;

    font: {
        weight: 400;
        size: 9px;
    }
}
</style>