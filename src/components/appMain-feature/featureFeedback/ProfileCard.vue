<script>
export default {
    data() {
        return {

        };
    },
    props: {
        profileImgUrl: {
            type: String,
            required: true
        },
        firstName: {
            type: String,
            required: true
        },
        lastName: {
            type: String,
            required: true
        },
        nationality: {
            type: String,
            required: true
        },
    }
};
</script>

<template>
    <!-- Profile Card  -->
    <div class="d-flex align-items-center gap-3" id="profile-card">
        <figure>
            <img :src="`/src/assets/${profileImgUrl}`" alt="profile img">
        </figure>
        <div class="data">
            <h6>{{ firstName }} {{ lastName }}</h6>
            <p>{{ nationality }}</p>
        </div>
    </div>
</template>

<style lang='scss' scoped>
img {
    width: 30px;
}

p {
    font-size: 14px;
    color: #94CB53;
}
</style>