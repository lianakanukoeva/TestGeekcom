<template>
    <UInput :input_title="title">
        <div class="counts">
            <div class="count" v-for="(item, k) in counts" :key="k">
                {{item}}
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
            counts: ["студия","1","2","3","4+"]
        }
    }
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
    &:last-child {
        border-right: 0;
    }
    &:hover {
        animation: count 1s;
        cursor: pointer;
    }
}
@keyframes count
{
    0%
    {
        transform: scale( 1 );
        color: #000;
    }
    20%
    {
            transform: scale( 1.15 );
        color: #000;
    }
    40%
    {
        transform: scale( 1.2 );
        color: #000;
    }
}
</style>