<script setup lang="ts">
export interface iIcon {
    style?: 'far' | 'fas' | 'fad';
    code: string;
}

export interface iProps {
    icon?: iIcon;
};

const props = defineProps<iProps>();
</script>

<template>
    <span v-if="props.icon" :class="`${props.icon.style ? props.icon.style : 'far'} ${props.icon?.code}`"></span>
    <slot></slot>
</template>

<style scoped>
span.fas,
span.far,
span.fad {
    margin-right: 6px;
}
</style>