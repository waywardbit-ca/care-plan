<script setup lang="ts">
import { iList } from '../../components/controls/List.vue';
import Item, { iIcon } from '../../components/controls/Item.vue';
import { inject, ref } from 'vue';

export interface iListItem {
    icon?: iIcon;
    type?: 'bad';
    text?: string;
    subList?: iList;
};

const props = defineProps<iListItem>();
const direction = ref(inject('direction'));
</script>

<template>
    <li :class="{
        'list-inline-item': direction === 'horizontal',
        'text-danger': type === 'bad'
    }">
        <Item :icon="props.icon">
            <span v-if="props.text" v-html="props.text"></span>
            <template v-if="!props.text">
                <slot></slot>
            </template>
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