<script setup lang="ts">
import { useSlots } from 'vue';

export interface iIcon {
    style?: 'far' | 'fas' | 'fad';
    code: string;
}

export interface iProps {
    type?: 'bad' | 'basic' | 'caution' | 'default' | 'good' | 'info';
    icon?: iIcon;
};

const props = withDefaults(defineProps<iProps>(), {
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
        <div v-if="hasSlot('heading')" class="card-header p-2">
            <h3 class="mb-0">
                <span v-if="props.icon"
                    :class="`${props.icon.style ? props.icon.style : 'far'} ${props.icon.code}`"></span>
                <slot name="heading"></slot>
            </h3>
        </div>
        <div class="card-body p-2">
            <slot></slot>
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