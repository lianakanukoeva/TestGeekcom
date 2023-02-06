<template>
    <UInput :input_title="title">
        <input type="text" placeholder="Срок сдачи">
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

<style lang="scss" scoped>
input{
    position: relative;
    max-width: 100%;
    padding: 10px;
    border: 0;
    outline: 0;
}
</style>