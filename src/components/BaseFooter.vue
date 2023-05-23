<script>
export default {
    name: 'BaseFooter',
    // props: [ "linkList" ],
    props: {
        linkList: Array
    },
    data() {
        return {
            links: [
                { imgPath: '/images/buy-comics-digital-comics.png', name: "DIGITAL COMICS"},
                { imgPath: '/images/buy-comics-merchandise.png', name: "DC MERCHANDISE"},
                { imgPath: '/images/buy-comics-subscriptions.png', name: "SUBSCRIPTION"},
                { imgPath: '/images/buy-comics-shop-locator.png', name: "COMIC SHOP LOCATOR"},
                { imgPath: '/images/buy-dc-power-visa.svg', name: "DC POWER VISA"},
            ],
            shop: [
                { text: "Shop DC"},
                { text: "Shop DC Collectibles"},
            ],
            dc: [
                { text: "Terms Of Use"},
                { text: "Privacy policy (New)"},
                { text: "Ad Choices"},
                { text: "Advertising"},
                { text: "Jobs"},
                { text: "Subscriptions"},
                { text: "Talent Workshops"},
                { text: "CPSC Certificates"},
                { text: "Ratings"},
                { text: "Shop Help"},
                { text: "Contact Us"},
            ],
            sites: [
                { text: "DC"},
                { text: "MAD Magazine"},
                { text: "DC Kids"},
                { text: "DC Universe"},
                { text: "DC Power Visa"},
            ],
            social: [
                { imgPath: "/images/footer-facebook.png"},
                { imgPath: "/images/footer-twitter.png"},
                { imgPath: "/images/footer-youtube.png"},
                { imgPath: "/images/footer-pinterest.png"},
                { imgPath: "/images/footer-periscope.png"},
            ]
        }    
    }    
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="row">
                <div v-for="link in links" class="col my_p-50">
                    <a class="my_m-33 text-light d-flex align-items-center" href="">
                        <img :src=" link.imgPath " alt="">
                        <p> {{ link.name }} </p>
                    </a>
                </div>
            </div>
        </div>
        <div class="container-fluid my_bg ">
            <div class="container">
                <div class="row">
                    <div class="col-4 my_p-50">
                        <div class="row">
                            <div class="col ">
                                <h6 class="mb-4 text-light">DC COMICS</h6>

                                <div class="d-flex flex-column">
                                    <a v-for="link in linkList" href="">{{ link.text }}</a>
                                </div>
                                
                                <h6 class="text-light">SHOP</h6>

                                <div class="d-flex flex-column">
                                    <a v-for="link in shop" href="">{{ link.text }}</a>
                                </div>
                                
                            </div>
                            <div class="col">
                                <h6 class="mb-4 text-light">DC</h6>

                                <div class="d-flex flex-column">
                                    <a v-for="link in dc" href="">{{ link.text }}</a>
                                </div>
                            </div>
                            <div class="col">
                                <h6 class="mb-4 text-light">SITES</h6>

                                <div class="d-flex flex-column">
                                    <a v-for="link in sites" href="">{{ link.text }}</a>
                                </div>
                            </div>
                        </div>
                        
                    </div>
                    <div class="col-8 my_bg-dc">
                        
                    </div>
                </div>
            </div>
        </div>
        <div class="container-fluid my_bg-black">
            <div class="container">
                <div class="row justify-content-between my_h100">
                    <div class="col position-relative p-0">
                        <div class="my_center">
                            <button class="my_btn p-2 text-light ">
                            SIGN-UP NOW!
                            </button>
                        </div>
                        
                    </div>
                    <div class="col d-flex">
                        <div class="col d-flex align-items-center">
                            <a class="my_color-blue fs-6" href="">FOLLOW US</a>
                        </div>
                        <div v-for="icone in social" class="col d-flex justify-content-center align-items-center">
                            <a href="">
                                <img class="my_img-fluid" :src="icone.imgPath" alt="">
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        

    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

    footer{
        background-color: #0282f9;
    }
    .my_bg-black{
        background-color: $black;
    }
    .my_btn{
        border-color: #0282f9;
        background-color:#303030;
    }
    .my_color-blue{
        color: #0282f9;
    }
    .my_bg{
        background-image: url(/images/footer-bg.png);
    }
    .my_bg-dc{
        background-image: url(/images/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;
    }
    a{
        color: #959595;
        margin-bottom: 5px;
        font-weight: 600;
        text-decoration: none !important;
        font-size: 10px;
    }
    p{
        margin: 0;
        margin-left: 17px;
    }
    .my_p-50{
        padding: 50px 0;
    }
    img{
        height: 55px;
    }
    .my_img-fluid{
        width: 35px;
        height: auto;
    }
    .my_m-33{
        margin-left: 33px;
    }
    .my_center{
        margin: 0;
        position: absolute;
        top: 50%;
        -ms-transform: translateY(-50%);
        transform: translateY(-50%);
    }
    .my_h12{
        height: 100px;
    }
</style>