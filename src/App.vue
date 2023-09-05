<template>
  <div ref="receiverRef"></div>
</template>

<script setup>
import {getServerConfig, getRTCConfiguration} from "@/unitylib/config";
import {createDisplayStringArray} from "@/unitylib/stats.js";
import {VideoPlayer} from "@/unitylib/videoplayer.js";

import {onMounted, ref} from "vue";
const receiverRef = ref(null);
onMounted(async () => {
  await setup();
});
const setup = async () => {
  const res = await getServerConfig();
  useWebSocket = res.useWebSocket;
};
</script>
