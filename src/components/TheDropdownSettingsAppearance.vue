<template>
    <DropdownSettingsHeader
        title="Appearance"
        @back="$emit('select-menu', 'main')"
    />
    <section class="py-2">
        <div class="text-gray-500 text-xs p-3">
            Setting applies to this browser only
        </div>
        <ul class="max-h-96 overflow-auto">
            <DropdownSettingsListItem
                v-for="(themeName, themeId) in themes"
                :key="themeId"
                :label="themeName"
                :active="themeId === selectedThemeId"
                @click="selectedThemeId = themeId"
            />
        </ul>
    </section>
</template>

<script>
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";
import DropdownSettingsListItem from "./DropdownSettingsListItem.vue";

export default {
    components: {
        DropdownSettingsHeader,
        DropdownSettingsListItem,
    },
    emits: ["select-menu"],

    data() {
        return {
            selectedThemeId: 0,
            themes: ["Use device theme", "Dark theme", "Light theme"],
        };
    },
};
</script>
