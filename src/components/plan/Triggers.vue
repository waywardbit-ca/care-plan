<script setup lang="ts">
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="bad" :icon="{ code: 'fa-thumbs-down' }">
        <template v-slot:heading>Things I <strong><u>do not</u></strong> like</template>
        <ul class="list-unstyled">
            <li><span class="far fa-comments"></span> Multiple people talking at a time</li>
        </ul>
    </Panel>
</template>

<style scoped></style>