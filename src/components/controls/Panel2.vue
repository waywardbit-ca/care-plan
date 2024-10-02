<script setup lang="ts">
import List from '../../components/controls/List.vue';
import { iList } from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import { useSlots } from 'vue';

export interface iIcon {
    style?: 'far' | 'fas' | 'fad';
    code: string;
}

export interface iPanel {
    type?: 'bad' | 'basic' | 'caution' | 'default' | 'good' | 'info';
    heading?: string;
    icon?: iIcon;
    content?: iList[] | string
};

const props = withDefaults(defineProps<iPanel>(), {
    type: 'default'
});
const slots = useSlots();

// methods
const hasSlot = (name: string) => {
    return !!slots[name];
};
</script>

<template>
    <div class="mb-3" :class="{
        'card border-danger bg-danger-subtle': props.type === 'bad',
        'card': props.type === 'basic',
        'card border-warning bg-warning-subtle': props.type === 'caution',
        'card border-success bg-success-subtle': props.type === 'good',
        'card border-info bg-info-subtle': props.type === 'info'
    }">
        <div v-if="props.heading" class="card-header p-2">
            <h3 class="mb-0">
                <span v-if="props.icon"
                    :class="`${props.icon.style ? props.icon.style : 'far'} ${props.icon.code}`"></span>
                <span v-html="props.heading"></span>
            </h3>
        </div>
        <div v-if="!props.heading && hasSlot('heading')" class="card-header p-2">
            <h3 class="mb-0">
                <span v-if="props.icon"
                    :class="`${props.icon.style ? props.icon.style : 'far'} ${props.icon.code}`"></span>
                <slot name="heading"></slot>
            </h3>
        </div>
        <div class="card-body p-2">
            <template v-if="typeof props.content === 'string'">
                {{ props.content }}
            </template>
            <template v-if="Array.isArray(props.content)">
                <template v-for="list in props.content">
                    <List v-bind="list">
                        <template v-for="item in list.items">
                            <ListItem v-bind="item"></ListItem>
                        </template>
                    </List>
                </template>
            </template>
        </div>
    </div>
</template>

<style scoped>
span.fas,
span.far,
span.fad {
    margin-right: 10px;
}
</style>