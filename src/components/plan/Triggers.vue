<script setup lang="ts">
import List from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="bad" :icon="{ code: 'fa-thumbs-down' }">
        <template v-slot:heading>Things I <strong><u>do not</u></strong> like</template>
        <List>
            <ListItem :icon="{ code: 'fa-comments' }">Multiple people talking at a time</ListItem>
        </List>
    </Panel>
</template>

<style scoped></style>