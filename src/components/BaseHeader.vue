<script>
export default {
    name: 'BaseHeader',
    data() {
        return {
            links: [
                { text: "CHARACTERS"}, 
                { text: "COMICS"}, 
                { text: "MOVIES"}, 
                { text: "TV"}, 
                { text: "GAMES"},
                { text: "COLECTIBLES"}, 
                { text: "VIDEOS"}, 
                { text: "FANS"},
                { text: "NEWS"},
                { text: "SHOP"}
            ]
        }    
    }    
}
</script>

<template>
    <header>
        <div class="container  ">
            <div class="row  align-items-center py-3">
                <div class="col d-flex"><img src="/images/dc-logo.png" alt=""></div>
                <div class="col d-flex">
                    <a v-for="link in links" href="">{{ link.text }}</a>
                </div>
            </div>
        </div>
        
    </header>
</template>

<style scoped>
img{
    width: 80px;
    height: auto;
}
a{
    font-weight: 600;
    text-decoration: none !important;
    color: #1c1c1c;
    font-size: 10px;
    margin-left: 33px;
}
</style>