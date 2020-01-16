<template>
  <button @click="onClick" class="custom-button">
    <slot>{{buttonText}}</slot>
  </button>
</template>

<script>
export default {
  props: {
    onClick: {
      type: Function,
      required: true
    },
    buttonText: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="less">
@white: #ffffff;
@bg-color: #f97252;

.custom-button {
  -webkit-appearance: none;
  border: 2px solid @white;
  background: transparent;
  cursor: pointer;
  height: 64px;
  width: 240px;
  outline: none;
  text-transform: uppercase;
  letter-spacing: 0.3em;
  font-size: 1em;
  color: @white;
  
  &:hover {
      color: @bg-color;
      background: @white;
  }

}
</style>