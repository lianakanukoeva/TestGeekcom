<template>
    <div class="input-title">{{input_title}}</div>
    <div class="border-box">
        <slot></slot>
    </div>
</template>
<script>
export default {
  props: {
    input_title: String
  }
}
</script>
<style lang="scss" scoped>
.input-title {
    color: #A4A4A4;
    font-size: 14px;
}
.border-box{
    border: 1px solid #ccc;
    border-radius: 3px;
    padding: 10px;
    font-size: 14px;
    color: #A4A4A4;
    max-width: 200px;
}
</style>