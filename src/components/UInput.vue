<template>
  <div class="uinput">
      <div class="input-title">{{input_title}}</div>
      <div class="border-box">
          <slot></slot>
      </div>
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
.uinput {
  margin-top: 20px;
}
.input-title {
    color: #A4A4A4;
    font-size: 14px;
}
.border-box {
    max-width: 100%;
    width: 200px;
    max-height: 36px;
    border: 1px solid #ccc;
    border-radius: 3px;
    font-size: 14px;
    color: #A4A4A4;
    overflow: hidden;
}
</style>