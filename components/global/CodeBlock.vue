<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    active: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<template>
  <div class="code-block" :class="[active && 'active']">
    <slot />
  </div>
</template>

<style lang="scss">
.code-block {
  display: none;
}
.code-block.active {
  display: block;
  border-radius: 0 0 6px 6px;

  .line-numbers {
    @apply mt-0;
  }
}
</style>
