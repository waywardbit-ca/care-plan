<script setup lang="ts">
import List from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel type="bad" :icon="{ code: 'fa-face-angry' }">
        <template v-slot:heading>If I refuse care...</template>
        <List>
            <ListItem :icon="{ code: 'fa-octagon-exclamation' }" type="bad">STOP WHAT YOU ARE DOING</ListItem>
            <ListItem :icon="{ code: 'fa-circle-question' }">Am I safe?
                <List :indent="true">
                    <ListItem :icon="{ code: 'fa-face-sleeping' }">Let me rest/sleep</ListItem>
                    <ListItem :icon="{ code: 'fa-user-nurse' }">Inform the <abbr title="Registered Nurse">RN</abbr></ListItem>
                </List>
            </ListItem>
            <ListItem :icon="{ code: 'fa-circle-question' }">Am I unsafe?
                <List :indent="true">
                    <ListItem :icon="{ code: 'fa-thought-bubble' }">Think about why this is happening</ListItem>
                    <ListItem :icon="{ code: 'fa-clock' }">Advise that you'll be back at a certain time</ListItem>
                    <ListItem :icon="{ code: 'fa-user-nurse' }">Inform the <abbr title="Registered Nurse">RN</abbr></ListItem>
                    <ListItem :icon="{ code: 'fa-swap' }">Modify the approach upon return</ListItem>
                </List>
            </ListItem>
        </List>
    </Panel>
</template>

<style scoped></style>