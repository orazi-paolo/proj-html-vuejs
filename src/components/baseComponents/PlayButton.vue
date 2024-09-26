<script>
export default {
    data() {
        return {

        };
    },
};
</script>

<template>
    <div class="play-btn p-2" role="btn">
        <div class="play-icon bg-white d-flex justify-content-center align-items-center">
            <img src="../../assets/icon/play-icon.png" alt="play-icon">
        </div>
    </div>
</template>

<style lang='scss' scoped>
.play-btn {
    border-radius: 50%;
    border: 1px solid #06CB7B;

    .play-icon {
        width: 50px;
        height: 50px;
        border-radius: 50%;
    }
}
</style>