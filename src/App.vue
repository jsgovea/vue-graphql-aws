<template>
  <div id="app">
    <div id="nav">
      <Nav />
    </div>
    <!-- <Home /> -->
    <router-view></router-view>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";
import { mapActions } from "vuex";

export default {
  name: "App",
  components: {
    Nav,
  },
  mounted() {
    this.authAction();
  },
  methods: {
    ...mapActions("auth", ["authAction"]),
  },
};
</script>