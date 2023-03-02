<script>
import Card from './Card.vue'
export default{
    components:{
        Card
    },

    data(){
        return{
            cardComics: [
                {
                    "thumb": '/images/card-1.jpg',
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-2.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-3.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "/images/card-4.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-5.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-6.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-7.webp",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-8.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-9.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-10.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-11.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "/images/card-12.webp",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<template>
<div class="bg-hero">
    <div class="container">
        <div class="button">
            <p>current series</p>
        </div>
    </div>
</div>

<div class="hero">
    <div class="container">
        <div class="row">
            <div class="col" v-for="(element, index) in cardComics ">
                <Card :image="element.thumb" :text="element.series"/>
            </div>
        </div>
        <div class="button">
            <p>load more</p>
        </div>
    </div>
</div>
</template>

<style scoped lang="scss">
@use '../partials/style/variables.scss';
@use '../partials/style/mixins.scss' as*;

.hero{
    padding-top: 54px;
    padding-bottom: 20px;
    background-color: #1C1C1C;
}
.row{
    flex-wrap: wrap;
    row-gap: 50px;
    gap: 28px;
    padding: 0 14px;
}
.col{
    width: calc(100% / 6 - 140px / 6);
    gap: 10px;
}

.button{
    color: white;
    text-transform: uppercase;
    background-color: $color-comics;
    padding: 13px 60px;
    width: fit-content;
    font-weight: 600;
    margin: 0 auto;
    margin-top: 50px;
}


.bg-hero{
    background-image: url('/images/jumbotron.jpg');
    height: 400px;
    background-repeat: no-repeat;
    background-size: cover;
    
    .container{
        position: relative;
        height: 100%;
    }

    .button{
        font-size: 20px;
        position: absolute;
        left: 0;
        bottom: 0;
        transform: translateY(50%);
        padding: 13px 30px;
    }
}
</style>