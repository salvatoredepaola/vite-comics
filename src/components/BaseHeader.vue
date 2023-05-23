<script>
export default {
    name: 'BaseHeader',
    // props: ["linkList"],
    props: {
        linkList: Array
    }
    
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row  align-items-center py-3">
                <div class="col d-flex"><img src="/images/dc-logo.png" alt=""></div>
                <div class="col d-flex">
                    <a v-for="link in linkList" href="">{{ link.text }}</a>
                </div>
            </div>
        </div>
        
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

header{

    img{
        width: 80px;
        height: auto;
    }
    a {
        font-weight: 600;
        text-decoration: none !important;
        color: #1c1c1c;
        font-size: 10px;
        margin-left: 33px;

        &:hover {
            color: $blue;
            font-weight: 600;
            transform: scale(1.2);
        }
    }
}

</style>