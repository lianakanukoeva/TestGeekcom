<template>
    <button type="submit">
        <span class="button__line top"></span>
        <span class="button__line right"></span>
        <span class="button__line bottom"></span>
        <span class="button__line left"></span>
        Применить фильтр
    </button>
</template>

<style lang="scss" scoped>
button {
    position: relative;
    display: inline-block;
    max-width: 200px;
    width: 100%;
    padding: 15px;
    border: 0;
    outline: 0;
    color: #BE131B;
    overflow: hidden;
    transition: 0.2s;
    border-radius: 3px;
    cursor: pointer;
    .button__line{
        position: absolute;
        display: block;
    }
    .top{
        top: 0;
        left: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(90deg, transparent, #BE131B);
    }
    &:hover .top{
        left: 100%;
        transition: 1s;
        transition-delay: 0s;
    }
    .right{
        right: 0;
        top: -100%;
        height: 100%;
        width: 2px;
        background: linear-gradient(180deg, transparent, #BE131B);
    }
    &:hover .right{
        top: 100%;
        transition: 1s;
        transition-delay: 0.25s;
    }
    .bottom{
        bottom: 0;
        right: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(-90deg, transparent, #BE131B);
    }
    &:hover .bottom{
        right: 100%;
        transition: 1s;
        transition-delay: 0s;
    }
    .left{
        left: 0;
        bottom: -100%;
        height: 100%;
        width: 2px;
        background: linear-gradient(0, transparent, #BE131B);
    }
    &:hover .left{
        bottom: 100%;
        transition: 1s;
        transition-delay: 0.25s;
    }
    &:hover{
        background-color: #BE131B;
        color: white;
        transition-delay: 0.6s;
    }
}
</style>