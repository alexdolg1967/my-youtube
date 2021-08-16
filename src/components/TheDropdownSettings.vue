<template>
	<div
  class="opacity-0 group-hover:opacity-100 absolute top-9 -right-full sm:right-0 bg-white w-72 border border-t-0"
>
          <section class="py-2 border-b">
            <ul>
              <DropdownSettingsListItem label="Appearance: Light" icon="sun" with-sub-menu />
              <DropdownSettingsListItem label="Language: English" icon="translate" with-sub-menu />
              <DropdownSettingsListItem label="Location: Ukraine" icon="globeAlt" with-sub-menu />
              <DropdownSettingsListItem label="Settings" icon="cog"/>
              <DropdownSettingsListItem label="Your data in YouTube" icon="shieldCheck"/>
              <DropdownSettingsListItem label="Help" icon="questionMarkCircle"/>
              <DropdownSettingsListItem label="Send feedback" icon="chatAlt"/>
              <DropdownSettingsListItem label="Keyboard shortcuts" icon="calculator" />
            </ul>
          </section>
          <section class="py-2">
            <ul>
					<DropdownSettingsListItem label="Restricted Mode: Off" with-sub-menu />
            </ul>
          </section>
        </div>
</template>

<script>
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'
export default {
  components: {
    DropdownSettingsListItem
  }
}
</script>