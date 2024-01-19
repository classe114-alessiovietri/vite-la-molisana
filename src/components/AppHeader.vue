<script>
export default {
    data() {
        return {
            mainMenu: [
                {
                    label: 'Home',
                    link: '#',
                    active: false,
                },
                {
                    label: 'Prodotti',
                    link: '#',
                    active: true,
                },
                {
                    label: 'Chi Siamo',
                    link: '#',
                    active: false,
                },
                {
                    label: 'Contatti',
                    link: '#',
                    active: false,
                },
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
    <header>
        <div>
            <img src="../assets/img/la-molisana-logo.png" alt="La Molisana">
        </div>

        <ul>
            <li v-for="(singleLink, i) in mainMenu" :key="i">
                <a :class="{
                        'active': singleLink.active
                    }"
                    :href="singleLink.link">
                    {{ singleLink.label }}
                </a>
            </li>
        </ul>
    </header>
</template>

<style lang="scss" scoped>
// header
header {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 20px;

    // header > ul
    > ul {
        list-style: none;
        padding: 0;

        // header > ul li
        li {
            display: inline-block;

            // header > ul li > a
            > a {
                display: inline-block;
                padding: 20px 15px;
                color: black;
                text-decoration: none;
                font-weight: bold;
                transition: all .1s ease-in-out;
                
                // header > ul li > a:hover, header > ul li > a.active
                &:hover,
                &.active {
                    background-color: #DAE9FE;
                }
            }
        }
    }
}
</style>
