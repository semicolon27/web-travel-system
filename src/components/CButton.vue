<template>
  <button
    class="btn"
    :disabled="disabled"
    :class="[
      {
        'btn-active': active,
        'btn-outline': outline,
        'btn-block': block,
        loading: loading,
        'btn-wide': wide,
      },
      setButtonColor,
      setButtonSize,
    ]"
  >
    <slot></slot>
  </button>
</template>

<script lang="ts" setup>
const props = defineProps({
  color: String,
  size: String,
  active: Boolean,
  outline: Boolean,
  disabled: Boolean,
  block: Boolean,
  loading: Boolean,
  wide: Boolean,
});

const setButtonColor = (): String => {
  if (props.color == null) return "";
  return `btn-${props.color}`;
};

const setButtonSize = (): String => {
  if (props.size == null) return "";
  return `btn-${props.size}`;
};
</script>
