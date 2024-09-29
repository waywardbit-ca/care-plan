<script setup lang="ts">
import List from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="basic" :icon="{ code: 'fa-comments'}">
        <template v-slot:heading>Interaction</template>
        <List>
            <ListItem :icon="{ code: 'fa-hand-holding-heart'}">I respond better to a gentle, but firm, approach</ListItem>
            <ListItem :icon="{ code: 'fa-mars'}">Male staff members present helps me accept care easier</ListItem>
            <ListItem :icon="{ code: 'fa-hand-wave'}">Introduce yourself to me</ListItem>
            <ListItem :icon="{ code: 'fa-comment'}">Explain to me why you are here</ListItem>
            <ListItem :icon="{ code: 'fa-circle-question'}">Are my clothes wet?
                <List :indent="true">
                    <ListItem :icon="{ code: 'fa-hand-point-ribbon'}">Remind me that I need to be changed</ListItem>
                    <ListItem :icon="{ code: 'fa-hand-back-point-right'}">Show me the clean clothes I need to wear</ListItem>
                    <ListItem :icon="{ code: 'fa-comment'}">Explain to me why it is important to change clothes</ListItem>
                </List>
            </ListItem>
            <ListItem :icon="{ code: 'fa-warning'}">I will grab my blankets and won't let go!
                <List :indent="true">
                    <ListItem :icon="{ code: 'fa-bolt'}">Try your best to get the blankets off me smoothly and quickly before I grab them</ListItem>
                    <ListItem :icon="{ code: 'fa-socks'}">f I am unwilling to let go of my blankets, ask if you can lift them up to my waist to clean the bottom half of my body. I may be more willing to have care performed like this</ListItem>
                </List>
            </ListItem>
        </List>
    </Panel>
</template>

<style scoped></style>