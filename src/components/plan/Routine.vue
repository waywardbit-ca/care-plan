<script setup lang="ts">
import List from '../../components/controls/List.vue';
import ListItem from '../../components/controls/ListItem.vue';
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel :icon="{ code: 'fa-clock' }">
        <template v-slot:heading>Routine</template>
        <div class="row">
            <div class="col-12 col-md-3">
                <h4><span class="far fa-sunrise"></span> Morning</h4>
                <List>
                    <ListItem :icon="{ code: 'fa-face-sleeping' }">Let me sleep until after breakfast</ListItem>
                    <ListItem :icon="{ code: 'fa-door-open' }">Enter room 10 to 15 minutes before my care</ListItem>
                    <ListItem :icon="{ code: 'fa-window-frame' }">Open curtains upon entering so I can start to wake gradually</ListItem>
                    <ListItem :icon="{ code: 'fa-heart' }">Try good incentives to get me up: coffee and ice cream</ListItem>
                </List>
            </div>
            <div class="col-12 col-md-3">
                <h4><span class="far fa-sun"></span> Daytime</h4>
            </div>
            <div class="col-12 col-md-3">
                <h4><span class="far fa-sunset"></span> Evening</h4>
            </div>
            <div class="col-12 col-md-3">
                <h4><span class="far fa-moon"></span> Nightime</h4>
            </div>
        </div>
    </Panel>
</template>

<style scoped></style>