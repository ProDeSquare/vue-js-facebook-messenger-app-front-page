<template>
  <div class="home py-4">
    <Chat :user="user" />
  </div>
</template>

<script>
import Chat from "@/components/chats/Chat";

export default {
  name: "home",
  props: ["user"],
  components: {
    Chat
  }
};
</script>
