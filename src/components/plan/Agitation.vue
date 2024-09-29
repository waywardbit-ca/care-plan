<script setup lang="ts">
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="caution" :icon="{code:'fa-face-diagonal-mouth'}">
        <template v-slot:heading>If I'm agitated...</template>
        <ul class="list-unstyled list-inline">
            <li class="list-inline-item"><span class="far fa-wrench"></span> Use the <mark><strong>Stop & Go</strong></mark> approach</li>
        </ul>
    </Panel>
</template>

<style scoped></style>