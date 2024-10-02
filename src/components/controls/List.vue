<script setup lang="ts">
import { iListItem } from '../../components/controls/ListItem.vue';
import { provide } from 'vue';

export interface iList {
    direction?: 'horizontal' | 'vertical';
    unstyled?: boolean;
    indent?: boolean;
    text?: string,
    items?: (iList | iListItem)[]
};

const props = withDefaults(defineProps<iList>(), {
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
:deep(li.list-inline-item) {
    margin-right: 10px
}
</style>