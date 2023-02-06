<template>
    <div class="card">
        <div class="card__img">
            <img :src="require(`@/assets/${img}`)" alt="">
            <div class="card__sale">{{ sale }}</div>
            <span class="card__sale-left"></span>
            <button class="card__heartbox" 
                :class="{ active: isActive }"
                @click = "classToggle">
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
    },
    data() {
        return {
            isActive: false
        }
    },
    methods: {
        classToggle(){
            this.isActive = !this.isActive;
        }
    }
}
</script>

<style lang="scss" scoped>
.card {
    position: relative;
    max-width: 250px;
    overflow: hidden;
    padding: 0;
    border-radius: 5px;
    margin-bottom: 50px;
    cursor: pointer;
    &:hover {
        transition: 0.5s;
        box-shadow: 0px 5px 15px 5px #ccc;
        transform: scale(1.02);
        .card__sale {
            transition: 0.5s;
            left: 0%;
        }
    }
}
.card__img img{
    display: block;
    position: relative;
    width: 100%;
    object-fit: cover;
}
.card__sale{
    width: 80px;
    background: #BE131B;
    position: absolute;
    color: #eee;
    padding: 5px;
    font-size: 12px;
    top: 10%;
    left: -30%;
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
    &:hover {
        animation: heartbeat 0.6s;
        .card__like {
            transition: 1s;
            background-color: #cc5d62;
            border: 2px solid #cc5d62;
        }
        .card__like:before,
        .card__like:after {
            transition: 1s;
            background-color: #cc5d62;
        }
    }
}
.card__heartbox.active {
    .card__like {
        transition: 1s;
        background-color: #BE131B;
        border: 2px solid #BE131B;
    }
    .card__like:before,
    .card__like:after {
        transition: 1s;
        background-color: #BE131B;
    }
    &:hover {
        animation: 0;
    }
}
.card__like {
    background-color: #ccc;
    border: 2px solid #ccc;
    display: inline-block;
    height: 10px;
    margin: 0 10px;
    position: relative;
    top: 2px;
    left: -6px;
    transform: rotate(-45deg);
    width: 13px;
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
    left: 5px;
    top: -4px;
}

.card__like:after {
    top: -11px;
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
    }
    20%
    {
        transform: scale( 1.25 )
    }
    40%
    {
        transform: scale( 1.5 )
    }
}
</style>