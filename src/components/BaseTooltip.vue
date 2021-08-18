<template>
   <div class="relative">
      <div
         class="h-full flex items-center"
         @mouseenter="isShow = true"
         @mouseleave="isShow = false"
         @click="isShow = false"
      >
         <slot />
      </div>
      <transition
         enter-active-class="duration-200"
         enter-from-class="opacity-0"
         enter-to-class="opacity-100"
         leave-active-class="duration-75"
         leave-from-class="opacity-100"
         leave-to-class="opacity-0"
      >
         <div v-show="isShow" :class="classes">{{ text }}</div>
      </transition>
   </div>
</template>

<script>
export default {
   props: {
      text: {
         type: String,
         default: 'Подсказка'
      },
      top: {
         type: Boolean,
         default: false
      },
		right:{
			type: Boolean,
         default: false
		},
		left:{
			type: Boolean,
         default: false
		}
   },
   data () {
      return {
         isShow: false,
			classes: [
            'bg-gray-600',
            'bg-opacity-80',
            'rounded-sm',
            'text-white',
            'text-xs',
            'whitespace-nowrap',
            'p-2',
            'absolute',
            'transform',
				... this.getPositionClasses()
         ]
      }
   },
	methods: {
		getPositionClasses() {
			const topClass = this.top ? 'bottom-8' : 'top-12'

			if (this.right) {
				return [topClass, 'left-0']
			}

			if (this.left) {
				return [topClass, 'right-0']
			}

			return [topClass, 'left-1/2', '-translate-x-1/2' ]
			
		}
	},
}
</script>
