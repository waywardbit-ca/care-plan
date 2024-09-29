<script setup lang="ts">
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="good" :icon="{ code: 'fa-heart' }">
        <template v-slot:heading>
            Things I <strong><span class="text-success">really</span></strong> like
        </template>
        <ul class="list-unstyled list-inline">
            <li class="list-inline-item"><span class="far fa-music"></span> Music</li>
            <li class="list-inline-item"><span class="far fa-guitar"></span> Guitar</li>
            <li class="list-inline-item"><span class="far fa-coffee"></span> Coffee</li>
            <li class="list-inline-item"><span class="far fa-ice-cream"></span> Ice Cream</li>
        </ul>
    </Panel>
</template>

<style scoped></style>