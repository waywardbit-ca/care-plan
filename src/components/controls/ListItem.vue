<script setup lang="ts">
import Item, { iIcon } from '../../components/controls/Item.vue';
import { inject, ref } from 'vue';

export interface iProps {
    icon?: iIcon;
    type?: 'bad';
};

const props = defineProps<iProps>();
const direction = ref(inject('direction'));
</script>

<template>
    <li :class="{
        'list-inline-item' : direction === 'horizontal',
        'text-danger': type === 'bad'
    }">
        <Item :icon="props.icon">
            <slot></slot>
        </Item>
    </li>
</template>

<style scoped>
span.fas,
span.far,
span.fad {
    margin-right: 10px;
}
</style>