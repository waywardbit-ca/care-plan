<script setup lang="ts">
import { provide } from 'vue';

export interface iProps {
    direction?: 'horizontal' | 'vertical';
    unstyled?: boolean;
    indent?: boolean;
};

const props = withDefaults(defineProps<iProps>(), {
    direction: 'vertical',
    unstyled: true,
    indent: false
});

provide("direction", props.direction);
</script>

<template>
    <ul class="mb-0" :class="{
        'list-unstyled': props.unstyled,
        'list-inline': props.direction === 'horizontal',
        'ms-4': props.indent === true
    }">
        <slot></slot>
    </ul>
</template>

<style scoped>
:deep(li.list-inline-item + li.list-inline-item) {
    margin-left: 10px
}
</style>