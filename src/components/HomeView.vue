<script setup lang="ts">
import Approach from './plan/Interaction.vue';
import Glimmers from '../components/plan/Glimmers.vue';
import Profile from '../components/plan/Profile.vue';
import Triggers from '../components/plan/Triggers.vue';
import Routine from '../components/plan/Routine.vue';
import Agitation from '../components/plan/Agitation.vue';
import Refusal from '../components/plan/Refusal.vue';
import Panel from '../components/controls/Panel2.vue';
import { iPanel } from '../components/controls/Panel2.vue';
import { ref } from 'vue';

const panels = ref<iPanel[]>([{
    type: 'basic',
    content: 'Stuff.'
},{
    type: 'good',
    icon: {
        code: 'fa-heart',
        style: 'far'
    },
    heading: 'Things I <span class="text-success">really</span> like',
    content: [{
        direction: 'horizontal',
        items: [{
            icon: {
                code: 'fa-music',
                style: 'far'
            },
            text: 'Music'
        },{
            icon: {
                code: 'fa-guitar',
                style: 'far'
            },
            text: 'Guitar'
        },{
            icon: {
                code: 'fa-coffee',
                style: 'far'
            },
            text: 'Coffee'
        },{
            icon: {
                code: 'fa-ice-cream',
                style: 'far'
            },
            text: 'Ice cream'
        }]
    }]
},{
    type: 'bad',
    icon: {
        code: 'fa-thumbs-down',
        style: 'far'
    },
    heading: 'Things I <u>do not</u> like',
    content: [{
        direction: 'horizontal',
        items: [{
            icon: {
                code: 'fa-comments',
                style: 'far'
            },
            text: 'Multiple people talking at a time'
        }]
    }]
}])
</script>

<template>
    <h2 class="h1"><span class="far fa-hand-wave"></span> Hi, my name is <span class="text-primary">Name</span>.</h2>
    <template v-for="panel in panels">
        <Panel v-bind="panel"></Panel>
    </template>
    <Profile></Profile>
    <div class="row">
        <div class="col-12 col-md-6">
            <Glimmers></Glimmers>
        </div>
        <div class="col-12 col-md-6">
            <Triggers></Triggers>
        </div>
    </div>
    <div class="row">
        <div class="col-12">
            <Routine></Routine>
        </div>
    </div>
    <div class="row">
        <div class="col-12 col-md-6">
            <Agitation></Agitation>
            <Refusal></Refusal>
        </div>
        <div class="col-12 col-md-6">
            <Approach></Approach>
        </div>
    </div>
</template>

<style scoped></style>