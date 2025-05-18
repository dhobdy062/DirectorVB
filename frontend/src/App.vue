<script setup>
import { ChatInterface } from "@videodb/chat-vue";
import "@videodb/chat-vue/dist/style.css";

// pull in your env vars
const socketUrl = import.meta.env.VITE_SOCKET_URL;
const httpUrl   = import.meta.env.VITE_HTTP_URL;
</script>

<template>
  <div class="h-screen">
    <ChatInterface
      :chat-hook-config="{
        socketUrl: socketUrl,
        httpUrl: httpUrl,
        debug: true
      }"
    />
  </div>
</template> 
