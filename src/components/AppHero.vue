<script>
export default {
    data() {
        return {
            jumboUrl: 'meme'
        }
    },

    methods: {
        getMemeUrl(pickName) {
            const url = new URL(`../assets/${pickName}.png`, import.meta.url)

            return url.href
        }
    }
}
</script>



<template>
    <div class="container">
        <div class="jumbo">
            <img :src="getMemeUrl(jumboUrl)" alt="">
        </div>
    </div>
</template>

<style scoped>
.container {
    width: 100%;
    background-color: blue;
}

.jumbo {
    width: 60%;
    padding: 50px;
    margin: auto;
}

img {
    width: 100%;
}
</style>