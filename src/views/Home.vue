<template>
  <div class="home py-4">
    <div v-for="friend in friends" :key="friend.id">
      <Chat :user="friend" />
    </div>
  </div>
</template>

<script>
import Chat from "@/components/chats/Chat";

export default {
  name: "home",
  props: ["friends"],
  components: {
    Chat
  }
};
</script>
