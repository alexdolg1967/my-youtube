<template>
  <div class="py-3 flex space-x-3 overflow-auto text-sm whitespace-nowrap">
    <a href="#" :class="classes">{{ category }}</a>
  </div>
</template>

<script>
export default {
  props: ['category', 'isActive'],
  computed: {
    classes () {
      const classes = ['mx-1 px-3', 'py-1', 'transition', 'rounded-full', 'border']
      return this.isActive
        ? [
            ...classes,
            'border-gray-700',
            'bg-gray-600',
            'hover:bg-gray-500',
            'text-white'
          ]
        : [...classes, 'border-gray-300', 'bg-gray-100', 'hover:bg-gray-200']
    }
  }
}
</script>
