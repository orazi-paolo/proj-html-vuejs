<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="bg-blue-dark">
        <div class="container pt-4 pb-4">
            <p class="d-flex justify-content-center align-items-center">
                Copyright @ 2022<span>FUTIO</span>. All rights reserved.
            </p>
        </div>
    </div>

</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

.bg-blue-dark {
    background-color: #1c212e;

    p {
        margin-bottom: 0;
        font-size: 14px;
        color: $lightGray;

        span {
            color: $lightOliveGreen;
        }
    }
}
</style>