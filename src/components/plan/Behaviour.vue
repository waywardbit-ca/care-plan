<script setup lang="ts">
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="info" :icon="{ code: 'fa-circle-exclamation'}">
        <template v-slot:heading>I will grab my blankets and I won't let go!</template>
        <div class="card well bg-default p-1">
            <p>
                Try your best to get the blankets off me <mark>smoothly and quickly</mark> before I grab them. (Be mindful of my mood and agitation though).
            </p>
            <p class="mb-0">
                If I am unwilling to let go of my blankets, ask if you can lift them up to my waist to clean the bottom half of my body. I may be more willing to have care performed like this.
            </p>
        </div>
    </Panel>
</template>

<style scoped></style>