<script setup lang="ts">
import Approach from './plan/Interaction.vue';
import Glimmers from '../components/plan/Glimmers.vue';
import Profile from '../components/plan/Profile.vue';
import Triggers from '../components/plan/Triggers.vue';
import Routine from '../components/plan/Routine.vue';
import Agitation from '../components/plan/Agitation.vue';
import Refusal from '../components/plan/Refusal.vue';
</script>

<template>
    <h2 class="h1"><span class="far fa-hand-wave"></span> Hi, my name is <span class="text-primary">Name</span>.</h2>
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