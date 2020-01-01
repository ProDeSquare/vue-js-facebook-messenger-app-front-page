<template>
  <div id="app" class="bg-black w-full text-light">
    <div class="container">
      <div class="bg-black pb-4" id="topbar">
        <Topbar :user="user" :app="app" />
        <Search />
      </div>

      <router-view :user="user" />

      <TheNavigation />
    </div>
  </div>
</template>

<script>
import Topbar from "@/components/partials/topbar";
import Search from "@/components/partials/search";
import TheNavigation from "@/components/partials/TheNavigation";

export default {
  data() {
    return {
      app: {
        title: "Chats"
      },
      user: {
        name: "Hamza Mughal",
        username: "ProDeSquare",
        email: "thathamzamughal@gmail.com",
        avatar: "https://gravatar.com/avatar/82a887d00da8efdbb2f7622b77771e3d"
      }
    };
  },
  components: {
    Topbar,
    Search,
    TheNavigation
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Montserrat:500+700&display=swap");

#app {
  min-height: 100vh;
  font-family: "Montserrat", sans-serif;
  font-weight: 500;
  padding-bottom: 80px;
}

* {
  transition: all 0.1s ease;
}

#topbar {
  position: sticky;
  top: 0;
}

.container {
  margin: 0 auto;
  max-width: 375px !important;
}

.cp {
  cursor: pointer;
}

svg {
  display: inline-block;
}

button,
input {
  &:focus {
    outline: none;
  }
}

::placeholder {
  color: rgb(168, 168, 168) !important;
}
</style>
