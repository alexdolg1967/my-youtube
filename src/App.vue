<template>
  <TheHeader />
  <TheSidebarSmall />
  <TheSidebar />
  <TheSidebarMobile />
  <TheCategories />
	<TheVideos />
  
</template>

<script>

import TheHeader from './components/TheHeader.vue'
import TheSidebar from './components/TheSidebar.vue'
import TheSidebarMobile from './components/TheSidebarMobile.vue'
import TheSidebarSmall from './components/TheSidebarSmall.vue'
import TheCategories from './components/TheCategories.vue'
import TheVideos from './components/TheVideos.vue'

export default {
	components:{
		TheHeader,
		TheSidebar,
		TheSidebarMobile,
		TheSidebarSmall,
		TheCategories,
		TheVideos
	}
}
</script>