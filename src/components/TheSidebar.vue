<template>
   <aside :class="classes">
      <SidebarContent />
   </aside>
</template>

<script>
import SidebarContent from './SidebarContent.vue'

export default {
   components: {
      SidebarContent
   },
   props: {
      isOpen: Boolean
   },
   data () {
      return {
         sidebarState: null // normal  compact
      }
   },
   computed: {
      classes () {
         return [
            this.isOpen ? 'xl:block' : 'hidden',
            'w-64',
            'max-h-screen',
            'overflow-auto',
            'fixed',
            'top-0',
            'pt-12',
            'bg-white',
            'z-20'
         ]
      }
   },
   mounted () {
      if (window.innerWidth >= 768 && window.innerWidth < 1280) {
         this.sidebarState = 'compact'
      }

      if (window.innerWidth >= 1280) {
         this.sidebarState = 'normal'
      }
   }
}
</script>
