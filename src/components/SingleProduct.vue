<script>
export default {
    data() {
        return {
        };
    },
    props: {
        title: {
            type: String,
            default: '[NOME PRODOTTO]'
        },
        image: String
    }
}
</script>

<template>
    <div class="single-product">
        <div>
            <img :src="image" :alt="title">
        </div>

        <h2>
            {{ title }}
        </h2>
    </div>
</template>

<style lang="scss" scoped>
.single-product {
    padding: 20px;
    border: 1px solid black;
    text-align: center;
    background-color: white;

    > div:first-child {
        margin-bottom: 15px;
    }

    h2 {
        color: $special-color;
        font-size: 1rem;
    }
}
</style>