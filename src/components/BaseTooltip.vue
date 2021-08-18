<template>
   <div class="relative">
      <div class="h-full" @mouseenter="toggle" @mouseleave="toggle">
         <slot />
      </div>
      <div v-show="isShow" :class="Classes">{{ text }}</div>
   </div>
</template>

<script>
export default {
   props: {
      text: {
         type: String,
         default: 'Подсказка'
      }
   },
   data () {
      return {
         isShow: false
      }
   },
   computed: {
      Classes () {
         return [
            'bg-gray-600',
            'bg-opacity-80',
            'rounded-sm',
            'text-white',
            'text-xs',
            'whitespace-nowrap',
            'p-2',
            'absolute',
            'top-14',
            'left-1/2',
            'transform',
            '-translate-x-1/2'
         ]
      }
   },
   methods: {
      toggle () {
         this.isShow = !this.isShow
      }
   }
}
</script>
