<template>
    <div class="card">
        <div class="card__img">
            <img :src="require(`@/assets/${img}`)" alt="">
            <div class="card__sale">{{ sale }}</div>
            <span class="card__sale-left"></span>
            <button class="card__heartbox">
                <div class="card__like"></div>
            </button>
        </div>
        <div class="card__text">
            <div class="card__flat">{{ flat }}</div>
            <div class="card__area">{{ area }}</div>
            <div class="card__price">{{ price }}</div>
            <div class="card__address">{{ address }}</div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        sale: String,
        img: String,
        flat: String,
        area: String,
        price: String,
        address: String
    }
}
</script>

<style lang="scss" scoped>
.card {
    position: relative;
    width: 25%;
    max-width: 250px;
    overflow: hidden;
    padding: 0;
    border-radius: 5px;
}
.card__img img{
    display: block;
    position: relative;
    width: 100%;
    object-fit: cover;
}
.card__sale{
    width: 65px;
    background: #BE131B;
    position: absolute;
    color: #eee;
    padding: 5px;
    font-size: 12px;
    top: 10%;
    left: 0;
}
.card__sale:after{
    content: "";
    width: 0;
    height: 0;
    position: absolute;
    top: 0%;
    left: 87%;
    border: 1px solid transparent;
    border-top: 2px solid #BE131B;
    border-bottom: 20px solid transparent;
    border-right: 20px solid tranaparent;
    border-left: 20px solid #BE131B;
}

.card__sale:before{
    content: "";
    width: 0;
    height: 0;
    position: absolute;
    bottom: 0%;
    left: 85%;
    z-index: 100;
    border: 2px solid transparent;
    border-top: 15px solid transparent;
    border-bottom: 20px solid #BE131B;
    border-right: 10px solid transparent;
    border-left: 10px solid transparent;
}
// .card__sale-left{
//     display: block;
//     width: 10px;
//     height: 40px;
//     background: #BE131B;
//     position: absolute;
//     left: -10px;
//     top: 0;
// }
// .card__sale-left:after{
//     content: "";
//     position: absolute;
//     top: 30px;
//     left: -10px;
//     border: 10px solid transparent;
//     border-top: 10px solid transparent;
//     border-bottom: 10px solid transparent;
//     border-left: 10px solid transparent;
//     border-right: 10px solid #BE131B;
// }
.card__heartbox {
    position: absolute;
    width: 33px;
    height: 33px;
    background-color: #fff;
    border: 0;
    border-radius: 3px;
    outline: 0;
    cursor: pointer;
    top: 10px;
    right: 10px;
}
.card__like {
    animation: heartbeat 1s;
    background-color: #ccc;
    border: 2px solid #ccc;
    display: inline-block;
    height: 10px;
    margin: 0 10px;
    position: relative;
    top: 2px;
    left: -7px;
    transform: rotate(-45deg);
    width: 10px;
}

.card__like:before,
.card__like:after {
    content: "";
    background-color: #ccc;
    border-radius: 50%;
    height: 13px;
    position: absolute;
    width: 14px;
}

.card__like:before {
    left: 6px;
    top: -1px;
}

.card__like:after {
    top: -10px;
    left: -2px;
}
.card__text {
    padding: 20px;
    line-height: 1.42;
    background-color: #fff;
}
.card__price {
    font-size: 18px;
    color: #BE131B;
}
.card__address{
    font-size: 14px;
}
@keyframes heartbeat
{
    0%
    {
        transform: scale( 1 )
        rotate(-45deg);    
    }
    20%
    {
        transform: scale( 1.25 )
        rotate(-45deg);  
    }
    40%
    {
        transform: scale( 1.5 )
        rotate(-45deg);
    }
}
</style>