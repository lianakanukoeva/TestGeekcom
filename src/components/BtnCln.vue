<template>
    <div class="btn-clean">
        <button type="">
            <span class="left"></span>
            <span class="right"></span>
            <div>
            Очистить фильтр
            </div>
        </button>
    </div>
</template>

<style lang="scss" scoped>
.btn-clean {
    position: relative;
    max-width: 200px;
    width: 100%;
    &:hover {
        button {
            color: #BE131B;
        }
        span {
            background-color: #BE131B;
        }
    }
    span {
        position: absolute;
        content: "";
        width: 1px;
        height: 20px;
        left: 30px;
        top: 12px;
        background-color: #5f76eb;
    }
    .left {
        transform: rotate(45deg);
    }
    .right
    {
        transform: rotate(-45deg);
    }
    button {
        width: 100%;
        padding: 15px;
        border: 0;
        outline: 0;
        background: 0;
        color: #5f76eb;
        cursor: pointer;
    }
}
</style>