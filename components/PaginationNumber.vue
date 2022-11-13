<template>
    <div>
        <p class="div-container flex justify-center items-center cursor-pointer py-px" :style="activeNumber">
            {{content}}
        </p>
    </div>
</template>

<script>
    export default {
        props: {
            content: String,
            active: {
                type: Boolean,
                default: false,
            }
        },
        computed: {
            activeNumber(){
                if(this.active){
                    return {
                        backgroundColor: "#1E1E1E",
                        color: "#FFFFFF"
                    }
                }
            }
        }
    }
</script>

<style lang="scss" scoped>
.div-container {
    width: 17px;
    height: 17px;
    background-color: white;
    border: 1px solid rgba(30, 30, 30, 0.2);
    border-radius: 5px;
    margin-left: 6px;
}

p {
    font-weight: 500;
    font-size: 8px;
    color: #1E1E1E;
}
</style>