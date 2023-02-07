<template>
    <UInput :input_title="title">
        <div class="counts">
            <div class="count"
                v-for="(item, k) in counts" :key="k"
                :class="{'active' : activeEl===item && isActive==true}"
                @click="(activeEl=item) && (isActive = !isActive)">
                <input type="checkbox" id="count">
                <label for="count">{{item}}</label>
            </div>
        </div>
    </UInput>
</template>

<script>
import UInput from '@/components/UInput'
export default {
    components: {
        UInput
    },
    props: {
        title: String
    },
    data(){
        return{
            counts: ["студия","1","2","3","4+"],
            activeEl: "",
            isActive: false
        }
    },
}
</script>

<style lang="scss" scoped>
.counts {
    display: flex;
}
.count {
    position: relative;
    max-width: 20%;
    width: 20%;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: 1px solid #ccc;
    padding: 3px 6px;
    line-height: 1;
    text-align: center;
    word-break: break-all;
    cursor: pointer;
    input[type="checkbox"]:checked, 
    input[type="checkbox"]:not(:checked), 
    input[type="radio"]:checked, 
    input[type="radio"]:not(:checked) 
    {
        position: absolute;
        left: -9999px;
    }
    label {
        cursor: pointer;
        &:hover {
            animation: count 1s;
        }
    }
    &:last-child {
        border-right: 0;
    }
}
.count.active{
    transition: 1s;
    color: #fff;
    background-color: #BE131B;
}
@keyframes count
{
    0%
    {
        transform: scale( 1 );
    }
    20%
    {
        transform: scale( 1.15 );
    }
    40%
    {
        transform: scale( 1.2 );
    }
}
</style>