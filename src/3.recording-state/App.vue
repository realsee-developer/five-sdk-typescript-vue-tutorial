<template>
    <FiveProvider :work="work">
        <FiveCanvas :width="width" :height="height" />
        <ModeController />
        <LookAroundController />
        <RecorderController />
    </FiveProvider>
</template>

<script setup lang="ts">

import { FiveProvider, FiveCanvas } from "@realsee/five/vue";
import { ref } from "vue";
import { useWindowDemisions } from "./useWindowDemisions";
import ModeController from "./ModeController.vue";
import LookAroundController from "./LookAroundController.vue";
import RecorderController from "./RecorderController.vue";

const work = ref();
const workURL = "https://vrlab-public.ljcdn.com/release/static/image/release/five/work-sample/07bdc58f413bc5494f05c7cbb5cbdce4/work.json";

fetch(workURL).then(response => response.text()).then(text => work.value = text);
const { width, height } = useWindowDemisions();
</script>