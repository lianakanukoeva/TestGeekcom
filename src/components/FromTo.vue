<template>
    <UInput :input_title="title">
        <input type="text" name="from" id="" placeholder="от"> | 
        <input type="text" name="to" id="" placeholder="до">
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
input{
    position: relative;
    max-width: 45%;
    border: 0;
    outline: 0;
}
</style>