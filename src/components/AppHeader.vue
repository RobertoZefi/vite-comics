<script>
export default{
    data(){
        return{
            listItem: [
                'characters',
                'comics',
                'movies',
                'tv',
                'games',
                'collectibles',
                'videos',
                'fans',
                'news',
                'shop'
            ]
        }
    }
}
</script>

<template>  
<div class="container">
    <div class="row">
        <div class="col">
            <img src="/images/dc-logo.png" alt="">
        </div>

        <div class="col">
            <ul class="list">
                <li v-for="element in listItem">{{ element }}</li>
            </ul>
        </div>
    </div>
</div>

</template>

<style scoped lang="scss">
@use '../partials/style/variables.scss';
@use '../partials/style/mixins.scss' as*;

.container{
    padding: 20px 0;
}
.row{
    justify-content: space-between;
    align-items: center;
}
.list{
    display: flex;
    gap: 33px;

    li{
        text-transform: uppercase;
        font-size: 14px;
        color: $color-darkGray;
        /*position: relative;
        display: flex;
        flex-direction: column;

        &:hover{
            color: $color-comics;
        }

        &:hover::after{
            content: '';
            position: absolute;
            border-bottom: 2px solid $color-comics;
            width: 100%;
            bottom: 0;
        }*/
    }
}
</style>