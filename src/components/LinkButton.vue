<template>
  <button
    :class="{ 'opacity-50': disabled, 'pointer-events-none': disabled }"
    class="p-2 outline-none focus:outline-none">
    <span class="flex flex-nowrap items-baseline justify-center space-x-2">
      <Icon
        v-if="icon"
        :name="icon" />
      <slot>
        <span v-if="text">
          {{ text }}
        </span>
      </slot>
    </span>
  </button>
</template>

<script>
export default {
  name: 'LinkButton',
  props: {
    disabled: {
      type: Boolean,
      default: false
    },
    text: {
      type: String,
      default: 'Button'
    },
    icon: {
      type: String,
      default: null
    }
  }
}
</script>
