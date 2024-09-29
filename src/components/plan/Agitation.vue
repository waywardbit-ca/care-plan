<script setup lang="ts">
import List from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="caution" :icon="{code:'fa-face-diagonal-mouth'}">
        <template v-slot:heading>If I'm agitated...</template>
        <List>
            <ListItem :icon="{ code: 'fa-wrench' }">Use the <mark><strong>Stop & Go</strong></mark> approach</ListItem>
        </List>
    </Panel>
</template>

<style scoped></style>