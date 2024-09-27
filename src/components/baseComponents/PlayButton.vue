<script>
export default {
    data() {
        return {

        };
    },
};
</script>

<template>
    <div class="play">
        <div class="play-btn p-2" role="btn">
        </div>
        <div class="play-icon bg-white d-flex justify-content-center align-items-center">
            <img src="/src/assets/icon/play-icon.png" alt="play-icon">
        </div>
    </div>
</template>

<style lang='scss'>
.play {
    position: relative;
    display: inline-block;
    width: 60px;
    height: 60px;
}

.play-btn {
    border-radius: 50%;
    border: 1px solid #06CB7B;
    animation: breath 7s linear infinite;
    display: inline-block;
    position: absolute;
    width: 60px;
    height: 60px;
}

.play-icon {
    position: absolute;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

@keyframes breath {
    0% {
        transform: scale(1, 1);
    }

    25% {
        transform: scale(1.1, 1.1);
    }

    50% {
        transform: scale(1.2, 1.2);
    }

    75% {
        transform: scale(1.1, 1.1);
    }

    100% {
        transform: scale(1, 1);
    }
}

@media (max-width: 992px) {
    .btn-group .play-icon {
        left: 100%;
    }
}
</style>