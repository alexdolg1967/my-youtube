<template>
   <div class="relative -mt-1 ml-auto">
      <button
         @click="isOpen = !isOpen"
         class="ml-auto -mt-1 p-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
      >
         <BaseIcon name="dotsVertical" class="h-5 w-5" />
      </button>
      <transition
         enter-active-class="transition ease-out duration-100"
         enter-from-class="opacity-0 scale-95"
         enter-to-class="opacity-100 scale-100"
         leave-active-class="transition ease-in duration-75"
         leave-from-class="opacity-100 scale-100"
         leave-to-class="opacity-0 scale-95"
      >
         <div
            v-show="isOpen"
            ref="dropdown"
            @keydown.esc="isOpen = false"
            tabindex="-1"
            class="absolute top-9 -right-full sm:right-0 bg-white w-48 rounded shadow focus:outline-none"
         >
            <section class="py-2">
               <ul>
                  <VideoItemDropdownListItem
                     label="Add to queue"
                     icon="menuAlt3"
                  />
               </ul>
            </section>
         </div>
      </transition>
   </div>
</template>

<script>
import BaseIcon from './BaseIcon.vue'
import VideoItemDropdownListItem from './VideoItemDropdownListItem.vue'

export default {
   components: {
      BaseIcon,
      VideoItemDropdownListItem
   },
   data () {
      return {
         isOpen: false
      }
   },
   mounted () {
      window.addEventListener('click', event => {
         if (!this.$el.contains(event.target)) {
            this.isOpen = false
         }
      })
   },
   watch: {
      isOpen () {
         this.$nextTick(() => this.isOpen && this.$refs.dropdown.focus())
      }
   }
}
</script>
