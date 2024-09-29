<script setup lang="ts">
import List from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="good" :icon="{ code: 'fa-heart' }">
        <template v-slot:heading>
            Things I <strong><span class="text-success">really</span></strong> like
        </template>
        <List direction="horizontal">
            <ListItem :icon="{ code: 'fa-music' }">Music</ListItem>
            <ListItem :icon="{ code: 'fa-guitar' }">Guitar</ListItem>
            <ListItem :icon="{ code: 'fa-coffee' }">Coffee</ListItem>
            <ListItem :icon="{ code: 'fa-ice-cream' }">Ice cream</ListItem>
        </List>
    </Panel>
</template>

<style scoped></style>