<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="cols">
                <div class="logo-container">
                    <img src="/img/la-molisana-logo.png" alt="La Molisana">
                </div>

                <div>
                    <h4>
                        Pastificio
                    </h4>

                    <ul>
                        <li v-for="i in 5" :key="i">
                            <a href="#">
                                Link
                            </a>
                        </li>
                    </ul>
                </div>

                <div>
                    <h4>
                        Prodotti
                    </h4>

                    <ul>
                        <li v-for="i in 5" :key="i">
                            <a href="#">
                                Link
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    min-height: 300px;
    background-image: url('../assets/img/footer-montagne-bottom.jpg');
    background-size: 100% auto;
    background-repeat: no-repeat;
    background-position: bottom center;

    .cols {
        display: flex;

        > * {
            width: calc(100% / 3);
        }
    }

    .logo-container {
        padding-right: 40px;
    }

    h4 {
        color: #1F3161;
        text-transform: uppercase;
        font-weight: bold;
        margin-bottom: 10px;
    }

    ul {
        list-style: none;
        padding: 0;

        li {
            margin-bottom: 3px;

            a {
                color: gray;
                text-decoration: none;
                font-size: .8rem;
                display: inline-block;
            }
        }
    }
}
</style>
