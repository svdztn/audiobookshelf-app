<template>
  <div class="w-full">
    <p class="px-1 pb-1 text-sm font-semibold">{{ label }}</p>
    <ui-text-input v-model="inputValue" :disabled="disabled" :type="type" class="w-full px-4 py-2" />
  </div>
</template>

<script>
export default {
  props: {
    value: [String, Number],
    label: String,
    type: {
      type: String,
      default: 'text'
    },
    disabled: Boolean
  },
  data() {
    return {}
  },
  computed: {
    inputValue: {
      get() {
        return this.value
      },
      set(val) {
        this.$emit('input', val)
      }
    }
  },
  methods: {},
  mounted() {}
}
</script>