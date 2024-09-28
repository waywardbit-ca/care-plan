<script setup lang="ts"></script>

<template>
    <div class="card well p-1 mb-3 border-danger bg-danger-subtle">
        <h3><span class="far fa-face-angry"></span> If I refuse care...</h3>
        <ul class="list-unstyled">
            <li><span class="far fa-octagon-exclamation text-danger"></span> <strong class="text-danger">STOP</strong>
                what you are doing</li>
            <li><span class="far fa-question"></span> Ask yourself if I am I safe (not a risk to myself/others, no skin
                breakdown, etc.)?
                <ul class="list-unstyled">
                    <li><span class="far fa-check text-success"></span> Safe:
                        <ul>
                            <li><span class="far fa-face-sleeping"></span> Let me rest/sleep</li>
                            <li><span class="far fa-user-nurse"></span> Inform the <abbr title="Registered Nurse">RN</abbr></li>
                        </ul>
                    </li>
                    <li><span class="far fa-times text-danger"></span> Not safe:
                        <ul>
                            <li><span class="far fa-thought-bubble"></span> Think about why this is happening</li>
                            <li><span class="far fa-clock"></span> Advise that you'll be back at a certain time</li>
                            <li><span class="far fa-user-nurse"></span> Inform the <abbr title="Registered Nurse">RN</abbr></li>
                            <li><span class="far fa-swap"></span> Modify the approach upon return</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</template>

<style scoped></style>