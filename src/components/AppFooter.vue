<script>
export default{
    data(){
        return{
            gadget: [
                {
                    image: '/images/buy-comics-digital-comics.png',
                    text: 'digital comics',
                },{
                    image: '/images/buy-comics-merchandise.png',
                    text: 'dc merchandise',
                },{
                    image: '/images/buy-comics-subscriptions.png',
                    text: 'subscription',
                },{
                    image: '/images/buy-comics-shop-locator.png',
                    text: 'comic shop locator',
                },{
                    image: '/images/buy-dc-power-visa.svg',
                    text: 'dc power visa',
                }
            ],

            info: [

            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="gadget">
            <div class="container">
                <ul class="list">
                    <li v-for="element in gadget">
                        <img :src="element.image" alt="">
                        <p>{{ element.text }}</p>
                    </li>
                </ul>
            </div>
        </div>

        <div class="info">
            <div class="container">
                <img class="logo" src="/images/dc-logo-bg.png" alt="">
                <div class="row">
                    <div class="col">
                        <ul class="info__list">
                            <li>
                                <h3>dc comics</h3>
                            </li>
                            <li>
                                <p>Characters</p>
                            </li>
                            <li>
                                <p>Comics</p>
                            </li>
                            <li>
                                <p>Movies</p>
                            </li>
                            <li>
                                <p>TV</p> 
                            </li>
                            <li>
                                <p>Games</p> 
                            </li>
                            <li>
                                <p>Videos</p>
                            </li>
                            <li>
                                <p>News</p>
                            </li>
                        </ul>

                        <ul class="info__list">
                            <li class="title">
                                <h3>shop</h3>
                            </li>
                            <li>
                                <p>Shop DC</p>
                            </li>
                            <li>
                                <p>Shop DC Collectibles</p>
                            </li>
                        </ul>
                    </div>

                    <div class="col">
                        <ul class="info__list">
                            <li>
                                <h3>dc</h3>
                            </li>
                            <li>
                                <p>Terms Of Use</p>
                            </li>
                            <li>
                                <p>Privacy policy (news)</p>
                            </li>
                            <li>
                                <p>Ad Choices</p>
                            </li>
                            <li>
                                <p>Advertising</p> 
                            </li>
                            <li>
                                <p>Jobs</p> 
                            </li>
                            <li>
                                <p>Subscriptions</p>
                            </li>
                            <li>
                                <p>Tealent Workshops</p>
                            </li>
                            <li>
                                <p>CPSC Certificates</p>
                            </li>
                            <li>
                                <p>Ratings</p>
                            </li>
                            <li>
                                <p>Shop Help</p>
                            </li>
                            <li>
                                <p>Contact Us</p>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul class="info__list">
                            <li>
                                <h3>sites</h3>
                            </li>
                            <li>
                                <p>DC</p>
                            </li>
                            <li>
                                <p>MAD Magazine</p>
                            </li>
                            <li>
                                <p>DC Kids</p>
                            </li>
                            <li>
                                <p>DC Universe</p> 
                            </li>
                            <li>
                                <p>DC Power Visa</p> 
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <div class="social">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <p class="button">sign-up now!</p>
                    </div>
                    <div class="col__icon">
                        <h3>follow us</h3>
                        <div class="icon">
                            <img src="/images/footer-facebook.png" alt="">
                            <img src="/images/footer-twitter.png" alt="">
                            <img src="/images/footer-youtube.png" alt="">
                            <img src="/images/footer-pinterest.png" alt="">
                            <img src="/images/footer-periscope.png" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use '../partials/style/variables.scss';
@use '../partials/style/mixins.scss' as*;

.gadget{
    background-color: $color-comics;
    padding: 50px 0;
}
.list{
    display: flex;
    gap: 70px;
    justify-content: center;

    li{
        display: flex;
        align-items: center;
        color: white;
        text-transform: uppercase;
        font-size: 13px;
        gap: 15px;

        img{
            width: 45px;
        }
    }
}

.info{
    background-image: url('/images/footer-bg.jpg');
    background-size: cover;

    .container{
        position: relative;
    }

    .row{
        gap: 54px;
        padding: 40px 0;
    }
}

.logo{
    position: absolute;
    right: 0;
    top: -12%;
    z-index: 0;
}
.info__list{

    .title{
        padding-top: 15px;
    }

    h3{
        text-transform: uppercase;
        padding-bottom: 25px;
        color: white;
    }

    p{
        color: gray;
        padding-bottom: 13px;
        font-size: 15px ;
    }
}

.social{
    background-color: $color-darkGray;
    position: relative;
    .row{
        justify-content: space-between;
        align-items: center;
        padding: 30px 0;
    }

    .button{
        border: 2px solid $color-comics;
        padding: 18px 15px;
        text-transform: uppercase;
        color: white;
        font-size: 18px;
    }

    .col__icon{
        display: flex;
        gap: 28px;
        align-items: center;

        h3{
            text-transform: uppercase;
            font-size: 20px;
            color: $color-comics;
        }
        .icon{
            display: flex;
            gap: 18px;
        }
    }
}

</style>