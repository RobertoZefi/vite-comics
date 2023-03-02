<script>
export default{
props:{
    image: {
        type: String,
        reaquired: true,
    },
    text: {
        type: String,
        reaquired: true,
    }
}
}
</script>

<template>
<div class="card">
    <img :src="image" alt="">
    <h4 class="title">{{ text }}</h4>
</div>
</template>

<style lang="scss">

.card{
    img{
        aspect-ratio: 1;
        object-fit: cover;
    }
    .title{
        text-transform: uppercase;
        color: white;
        font-weight: 500;
        margin-top: 20px;
        font-size: 15px;
    }
}
</style>