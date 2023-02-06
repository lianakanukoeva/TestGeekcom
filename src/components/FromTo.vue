<template>
    <UInput :input_title="title">
        <div class="inputs">
            <input type="text" name="from" id="" placeholder="от"> | 
            <input type="text" name="to" id="" placeholder="до">
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
    }
}
</script>

<style scoped>
.inputs {
    position: relative;
    display: flex;
    align-items: center;
    max-width: 100%;
}
input{
    position: relative;
    display: block;
    max-width: 47%;
    padding: 10px;
    border: 0;
    outline: 0;
}
</style>