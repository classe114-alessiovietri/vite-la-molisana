<script>
import SingleProduct from './SingleProduct.vue';

export default {
    data() {
        return {
            pastas: [
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    titolo: "N.4 Spaghetto Quadrato Bucato",
                    tipo: "lunga",
                    cottura: 6,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                    titolo: "N.5 Fettuccine",
                    tipo: "lunga",
                    cottura: 13,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
                    titolo: "N.6 Linguine",
                    tipo: "lunga",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
                    titolo: "N.7 Mezze Linguine",
                    tipo: "lunga",
                    cottura: 11,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
                    titolo: "n.11 Spaghettino Quadrato",
                    tipo: "lunga",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
                    titolo: "N.38 Mezze maniche",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
                    titolo: "N.44 Sedani",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
                    titolo: "N.49 Sedanini",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
                    titolo: "N.53 Lumachine",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
                    titolo: "N.55 Chifferi rigati",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
                    titolo: "N.58 Misto corto",
                    tipo: "corta",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
                    titolo: "N.84 Ditale Quadrato",
                    tipo: "cortissima",
                    cottura: 12,
                },
            ],
            breads: [
                {
                    img: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    name: "Pane Bianco"
                },
                {
                    img: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
                    name: "Pane Senza Glutine"
                }
            ]
        };
    },
    components: {
        SingleProduct
    }
}
</script>

<template>
    <main>
        <div class="container">
            <h1>
                Lista Prodotti
            </h1>

            <div class="products-container">
                <SingleProduct
                    class="width-25"
                    v-for="(pasta, i) in pastas"
                    :key="i"
                    :title="pasta.titolo"
                    :image="pasta.src" />
            </div>

            <hr>

            <h1>
                Lista Pani
            </h1>

            <div class="products-container">
                <SingleProduct
                    class="width-50"
                    v-for="(bread, i) in breads"
                    :key="i"
                    :title="bread.name"
                    :image="bread.img" />
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
.width-25 {
    width: 25%;
}

.width-50 {
    width: 50%;
}

main {
    background-image: url('/img/fondo-pag-speciali.jpg');
    background-size: 100% auto;
    margin-bottom: 20px;
    padding: 50px 0;

    h1 {
        text-align: center;
        color: #0F346F;
        margin-bottom: 20px;
    }

    .products-container {
        display: flex;
        flex-wrap: wrap;

        // .single-product {
        //     width: 25%;
        //     padding: 20px;
        //     border: 1px solid black;
        //     text-align: center;
        //     background-color: white;

        //     > div:first-child {
        //         margin-bottom: 15px;
        //     }

        //     h2 {
        //         color: #0F346F;
        //         font-size: 1rem;
        //     }
        // }
    }
}
</style>
