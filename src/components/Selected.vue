<template>
    <UInput :input_title="title">
        <div class="select-wrapper">
            <select name="select-category" class="select">
                <option v-for="(li, k) in option_list" :key="k" :value="li.select_value">{{ li.title }}</option>
            </select>
        </div>
    </UInput>
</template>

<style lang="scss" scoped>
.select {
	width: 95%;
    opacity: 0.7;
	border: none;
	background-color: #fff;
    padding: 10px;
	outline: none;
	cursor: pointer;
}
</style>

<script>
import UInput from '@/components/UInput'
export default {
    components: {
        UInput
    },
    props: {
        title: String,
        option_list: Array
    }
}
</script> 