<script setup lang="ts">
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="basic" :icon="{ code: 'fa-comments'}">
        <template v-slot:heading>Interaction</template>
        <ul class="list-unstyled">
            <li><span class="far fa-handshake-angle"></span> <mark>Gentle but firm</mark> approach works best</li>
            <li><span class="far fa-hand-wave"></span> <mark>Introduce yourself</mark> and <mark>explain why</mark> you
                are here</li>
            <li><span class="far fa-hand-point-ribbon"></span> <mark>Remind me</mark> I need to be changed because my
                clothes are wet</li>
            <li><span class="far fa-hand-back-point-right"></span> <mark>Show me</mark> the clean clothes I need to wear
            </li>
            <li><span class="far fa-circle-question"></span> <mark>Explain why</mark> it is important to get changed</li>
            <li><span class="far fa-mars"></span><mark> Male staff members present helps</mark> make care easier
                (depends on mood and agreeableness)</li>
        </ul>
    </Panel>
</template>

<style scoped></style>