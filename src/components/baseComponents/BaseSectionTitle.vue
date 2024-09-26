<script>
export default {
    data() {
        return {

        }
    },
    props: {
        isCenter: {
            type: Boolean,
            default: false,
        },
        contentGreen: {
            type: String,
            required: true
        },
        mainTitle: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true,
        }

    },
}
</script>

<template>
    <div :class="{'text-center centralize' : isCenter}">
        <h5 class="subtitle">
            {{ contentGreen }}
        </h5>
        <h1>
            {{ mainTitle }}
        </h1>
        <p class="description">
            {{ description }}
        </p>
    </div>

</template>

<style lang="scss" scoped>
.centralize{
    margin: 0 auto;
    width: 50%;
}
div{

    .subtitle{
        color: #94CB53;
    }

    h1 {
        color: white;
    }

    p {
        color: #EBEBEB;
    }
}
</style>