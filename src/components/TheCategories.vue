<template>
  <section
    class="pt-14 md:pl-24 xl:pl-64 w-full fixed bg-white bg-opacity-95 z-10"
  >
    <div class="flex border-t border-b px-4 max-w-screen-2xl m-auto">
      <CategoryItem v-for="category in categories" :key="category" :category="category" :is-active = "category === 'All'"/>
    </div>
  </section>
</template>

<script>

import CategoryItem from './CategoryItem.vue'

export default {
	components:{
		CategoryItem
	},
  data () {
    return {
      categories: [
        'All',
        'Trucks',
        'Tools',
        'Mashines',
        'Engines',
        'Show',
        'Ships',
        'Roads',
        'Tanks'
      ]
    }
  }
}
</script>
