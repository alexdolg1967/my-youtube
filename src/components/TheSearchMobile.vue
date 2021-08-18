<template>
   <div class="fixed flex bg-white h-14 p-2 w-full z-10">
      <BaseTooltip text="Back" right>
         <button class="p-2 mr-2 focus:outline-none">
            <BaseIcon name="arrowLeft" class="w-5 h-5" />
         </button>
      </BaseTooltip>
      <TheSearch />
      <BaseTooltip text="Microphone" left>
         <button class="p-2 focus:outline-none">
            <BaseIcon name="microphone" class="w-5 h-5" />
         </button>
      </BaseTooltip>
   </div>
</template>

<script>
import BaseIcon from './BaseIcon.vue'
import BaseTooltip from './BaseTooltip.vue'
import TheSearch from './TheSearch.vue'

export default {
   components: {
      BaseIcon,
      BaseTooltip,
      TheSearch
   }
}
</script>
