<template>
  <div id="app" class="bg-black w-full text-light">
    <div class="container">
      <div class="bg-black pb-4" id="topbar">
        <Topbar :user="user" :app="app" />
        <Search />
      </div>

      <router-view :friends="friends" />

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
        id: 1,
        name: "Hamza Mughal",
        username: "ProDeSquare",
        email: "thathamzamughal@gmail.com",
        avatar: "https://gravatar.com/avatar/82a887d00da8efdbb2f7622b77771e3d"
      },
      friends: [
        {
          id: 2,
          name: "Hamza Mughal",
          username: "ProDeSquare",
          email: "thathamzamughal@gmail.com",
          avatar: "https://gravatar.com/avatar/82a887d00da8efdbb2f7622b77771e3d"
        },
        {
          id: 3,
          name: "Zeeshan Ghumman",
          username: "zeeshan",
          email: "zeeshan@gmail.com",
          avatar:
            "https://scontent.fkhi10-1.fna.fbcdn.net/v/t1.0-9/71642571_2394782360735706_2540505011356434432_n.jpg?_nc_cat=108&_nc_ohc=EQICWa0kg6sAQmrmCrB1snPIfQsSJNNy-xJYetQHBOxlYyHJvZmobmVwA&_nc_ht=scontent.fkhi10-1.fna&oh=579ebd1f8ab75cb117be6dd30728da13&oe=5EB45391"
        }
      ]
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
  max-width: 500px !important;
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
