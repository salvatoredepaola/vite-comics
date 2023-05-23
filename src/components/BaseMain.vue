<script>
export default {
    name: 'BaseMain',
    props: {
        fumetti: Array
    },
    mounted() {
        console.log(this.fumetti)
    }
}
</script>

<template>
    <main>
        <div class="container-fluid"><div class="row align-items-center my_height-112"></div></div>
        <div class="container-fluid my_bg-black p-5">
            <div class="container">
                <div class="row">
                    <div class="col d-flex flex-wrap justify-content-center">
                        <div v-for="comic in fumetti" class="card mb-2">
                            <img class="mb-3" :src="comic.thumb" :alt="comic.series">
                            <p class="text-light">
                                {{ comic.series }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

main{
    background-image: url(/images/jumbotron.png);
}
.my_height-112{
    height: 400px;
}
.my_bg-black{
        background-color: $black;
    }
    .card{
        width: 185px;
        // height: 185px;
        border: none;
        margin: 10px;
        border-radius: 0;
        background-color: $black;
        img{
            width: 100%; 
            height: 185px;
            object-fit: cover;
            object-position: 0 0;
        }
    }
</style>