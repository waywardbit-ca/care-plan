<script setup lang="ts">
import Panel from '../../components/controls/Panel.vue';
</script>

<template>
    <Panel :icon="{ code: 'fa-clock' }">
        <template v-slot:heading>Routine</template>
        <div class="row">
            <div class="col-12 col-md-3">
                <h4><span class="far fa-sunrise"></span> Morning</h4>
                <ul class="list-unstyled">
                    <li><span class="far fa-face-sleeping"></span> Let me sleep until <mark>after</mark> breakfast</li>
                    <li><span class="far fa-door-open"></span> Enter room <mark>10</mark> to <mark>15</mark> minutes
                        <mark>before</mark>my care
                    </li>
                    <li><span class="far fa-window-frame"></span> Open curtains <mark>upon</mark> entering so I can
                        start to
                        wake <mark>gradually</mark></li>
                    <li><span class="far fa-heart"></span> Try good incentives to get me up: <mark>coffee</mark> and
                        <mark>ice
                            cream</mark>
                    </li>
                </ul>
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