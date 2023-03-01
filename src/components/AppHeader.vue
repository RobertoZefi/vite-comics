<script>
export default{
    data(){
        return{
            
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
                <li>characters</li>
                <li>comics</li>
                <li>movies</li>
                <li>tv</li>
                <li>games</li>
                <li>collectibles</li>
                <li>videos</li>
                <li>fans</li>
                <li>news</li>
                <li>shop</li>
            </ul>
        </div>
    </div>
</div>

</template>

<style scoped lang="scss">
@use '../partials/style/variables.scss';

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
        font-size: 15px;
    }
}
</style>