<template>
    <nav class="navbar fixed-bottom navbar-light bg-light">
        <div class="container-fluid justify-content-center">
            <div class="btn-group">
                <button class="btn btn-primary active" @click="() => setState({mode: Five.Mode.Panorama})">全景漫游</button>
                <button class="btn btn-primary" @click="() => setState({mode: Five.Mode.Floorplan}) ">空间总览</button>
            </div>
        </div>
  </nav>
</template>

<script setup lang="ts">

import { useFiveCurrentState } from "@realsee/five/vue";
import { Five } from "@realsee/five";

const [, setState] = useFiveCurrentState();

</script>